## Class design

What of this can be got from sweet?

From our discussion:

	ads:FundingAgency
	ads:ObservationAgency
	ads:Proposal
		ads:ObservingProposal
	ads:FundingInitiative
	ads:FundingProgram
	ads:Grant (has a grant identifier)

	ads:Collaboration

And from ads:

    ads:Observatory
        ads:SpaceCraft
        ads:GroundBasedObservatory
    ads:Instrument
        ads:Telescope
    ads:Observation
    --ads:DataArchive
    ads:Dataset
    ads:DataProduct

Should we be dealing with co-ordinates at all? Dosent seem sweet provides us
much useful stuff; and we can always connect to sweet later. Why would we want this?
Its for Alyssa's heat maps, object positions, field layers etc. But how do we
define without going into a complete nutness about co-ordinate systems? Or perhaps
just deal with objects and concepts, not the floats associated with it.

The kind of object should be in the object ontology, as well as position and such.
At this level we only need to know something about the sky.

So should we:

	ads:AstronomicalObject
	ads:RegionOfSky
		ads:ObservationField

    ads:GeographicBoundingBox

Dont we want something more with the coords and time???

In addition to this we import sweet into ads base
foaf will be impoted, and by that also dc

we'll import skos into biblio with the aakeys.
