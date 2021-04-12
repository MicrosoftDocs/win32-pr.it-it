---
title: Identificatori di interfaccia
description: Identificatori di interfaccia
ms.assetid: 009edcc0-34db-40a1-ae76-17492b11604a
keywords:
- Windows Media Format SDK, identificatori di interfaccia (IID)
- Advanced Systems Format (ASF), identificatori di interfaccia (IID)
- ASF (formato avanzato dei sistemi), identificatori di interfaccia (IID)
- identificatori di interfaccia (IID)
- IID (identificatori di interfaccia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253ca5b4110536c2207f7e18ab0f28067789df71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331599"
---
# <a name="interface-identifiers"></a>Identificatori di interfaccia

È necessario usare un identificatore di interfaccia (IID) quando si effettuano chiamate al metodo **QueryInterface** . Un IID è un valore di identificatore univoco globale (GUID). In Windows Media Format SDK, la costante assegnata all'IID per una data interfaccia è il nome dell'interfaccia preceduta da "IID \_ ".

Nella tabella seguente sono elencati gli identificatori di interfaccia e le costanti associate per le interfacce in questo SDK.



| Interfaccia                       | IID (costante)                     | GUID                                 |
|---------------------------------|----------------------------------|--------------------------------------|
| **INSSBuffer**                  | \_INSSBUFFER IID                  | E1CD3524-03D7-11d2-9EED-006097D2D7CF |
| **INSSBuffer2**                 | \_INSSBUFFER2 IID                 | 4f528693-1035-43fe-b428-757561ad3a68 |
| **INSSBuffer3**                 | \_INSSBUFFER3 IID                 | c87ceaaf-75be-4bc4-84eb-ac2798507672 |
| **INSSBuffer4**                 | \_INSSBUFFER4 IID                 | b6b8fd5a-32e2-49d4-a910-c26cc85465ed |
| **IWMAddressAccess**            | \_IWMADDRESSACCESS IID            | BB3C6389-1633-4E92-AF14-9F3173BA39D0 |
| **IWMAddressAccess2**           | \_IWMADDRESSACCESS2 IID           | 65A83FC2-3E98-4D4D-81B5-2A742886B33D |
| **IWMBackupRestoreProps**       | \_IWMBACKUPRESTOREPROPS IID       | 3C8E0DA6-996F-4ff3-A1AF-4838F9377e2e |
| **IWMBandwidthSharing**         | \_IWMBANDWIDTHSHARING IID         | ad694af1-f8d9-42f8-bc47-70311b0c4f9e |
| **IWMClientConnections**        | \_IWMCLIENTCONNECTIONS IID        | 73c66010-a299-41df-b1f0-ccf03b09c1c6 |
| **IWMClientConnections2**       | \_IWMCLIENTCONNECTIONS2 IID       | 4091571e-4701-4593-bb3d-d5f5f0c74246 |
| **IWMCodecInfo**                | \_IWMCODECINFO IID                | a970f41e-34de-4a98-b3ba-e4b3ca7528f0 |
| **IWMCodecInfo2**               | \_IWMCODECINFO2 IID               | aa65e273-b686-4056-91ec-dd768d4df710 |
| **IWMCodecInfo3**               | \_IWMCODECINFO3 IID               | 7e51f487-4d93-4f98-8ab4-27d0565adc51 |
| **IWMCredentialCallback**       | \_IWMCREDENTIALCALLBACK IID       | 342e0eb7-e651-450c-975b-2ace2c90c48e |
| **IWMDeviceRegistration**       | \_IWMDEVICEREGISTRATION IID       | f6211f03-8d21-4e94-93e6-8510805f2d99 |
| **IWMDRMEditor**                | \_IWMDRMEDITOR IID                | FF130EBC-A6C3-42A6-B401-C3382C3E08B3 |
| **IWMDRMMessageParser**         | \_IWMDRMMESSAGEPARSER IID         | a73a0072-25a0-4c99-b4a5-ede8101a6c39 |
| **IWMDRMReader**                | \_IWMDRMREADER IID                | d2827540-3ee7-432c-b14c-dc17f085d3b3 |
| **IWMDRMReader2**               | \_IWMDRMREADER2 IID               | befe7a75-9f1d-4075-b9d9-a3c37bda49a0 |
| **IWMDRMReader3**               | \_IWMDRMREADER3 IID               | f28c0300-9baa-4477-A846-1744d9cbf533 |
| **IWMDRMTranscryptor**          | \_IWMDRMTRANSCRYPTOR IID          | 69059850-6e6f-4bb2-806f-71863ddfc471 |
| **IWMDRMWriter**                | \_IWMDRMWRITER IID                | D6EA5DD0-12A0-43F4-90AB-A3FD451E6A07 |
| **IWMDRMWriter2**               | \_IWMDRMWRITER2 IID               | 38ee7a94-40e2-4e10-aa3f-33fd3210ed5b |
| **IWMDRMWriter3**               | \_IWMDRMWRITER3 IID               | a7184082-a4aa-4dde-ac9c-e75dbd1117ce |
| **IWMHeaderInfo**               | \_IWMHEADERINFO IID               | 96406bda-2b2b-11d3-b36b-00c04f6108ff |
| **IWMHeaderInfo2**              | \_IWMHEADERINFO2 IID              | 15cf9781-454e-482e-b393-85fae487a810 |
| **IWMHeaderInfo3**              | \_IWMHEADERINFO3 IID              | 15CC68E3-27CC-4ecd-B222-3F5D02D80BD5 |
| **IWMImageInfo**                | \_IWMIMAGEINFO IID                | 9F0AA3B6-7267-4D89-88F2-BA915AA5C4C6 |
| **IWMIndexer**                  | \_IWMINDEXER IID                  | 6d7cdc71-9888-11d3-8edc-00c04f6109cf |
| **IWMIndexer2**                 | \_IWMINDEXER2 IID                 | b70f1e42-6255-4df0-a6b9-02b212d9e2bb |
| **IWMInputMediaProps**          | \_IWMINPUTMEDIAPROPS IID          | 96406bd5-2b2b-11d3-b36b-00c04f6108ff |
| **IWMIStreamProps**             | \_IWMISTREAMPROPS IID             | 6816dad3-2b4b-4c8e-8149-874c3483a753 |
| **IWMLanguageList**             | \_IWMLANGUAGELIST IID             | DF683F00-2D49-4D8E-92B7-FB19F6A0DC57 |
| **IWMLicenseBackup**            | \_IWMLICENSEBACKUP IID            | 05E5AC9F-3FB6-4508-BB43-A4067BA1EBE8 |
| **IWMLicenseRestore**           | \_IWMLICENSERESTORE IID           | C70B6334-a22e-4efb-A245-15E65A004A13 |
| **IWMLicenseRevocationAgent**   | \_IWMLICENSEREVOCATIONAGENT IID   | 6967f2c9-4e26-4b57-8894-799880f7ac7b |
| **IWMMediaProps**               | \_IWMMEDIAPROPS IID               | 96406bce-2b2b-11d3-b36b-00c04f6108ff |
| **IWMMetadataEditor**           | \_IWMMETADATAEDITOR IID           | 96406bd9-2b2b-11d3-b36b-00c04f6108ff |
| **IWMMetadataEditor2**          | \_IWMMETADATAEDITOR2 IID          | 203cffe3-2e18-4fdf-b59d-6e71530534cf |
| **IWMMutualExclusion**          | \_IWMMUTUALEXCLUSION IID          | 96406bde-2b2b-11d3-b36b-00c04f6108ff |
| **IWMMutualExclusion2**         | \_IWMMUTUALEXCLUSION2 IID         | 302b57d?-89d1-4ba2-85c9-166f2c53eb91 |
| **IWMOutputMediaProps**         | \_IWMOUTPUTMEDIAPROPS IID         | 96406bd7-2b2b-11d3-b36b-00c04f6108ff |
| **IWMPacketSize**               | \_IWMPACKETSIZE IID               | cdfb97ab-188f-40b3-b643-5b7903975c59 |
| **IWMPacketSize2**              | \_IWMPACKETSIZE2 IID              | 8bfc2b9e-B646-4233-A877-1c6a7? 9669dc |
| **IWMPlayerHook**               | \_IWMPLAYERHOOK IID               | e5b7ca9a-0f1c-4f66-9002-74ec50d8b304 |
| **IWMProfile**                  | \_IWMPROFILE IID                  | 96406bdb-2b2b-11d3-b36b-00c04f6108ff |
| **IWMProfile2**                 | \_IWMPROFILE2 IID                 | 07e72d33-d94e-4be7-8843-60ae5ff7e5f5 |
| **IWMProfile3**                 | \_IWMPROFILE3 IID                 | 00ef96cc-a461-4546-8bcd-c9a28f0e06f5 |
| **IWMProfileManager**           | \_IWMPROFILEMANAGER IID           | d16679f2-6ca0-472d-8d31-2f5d55aee155 |
| **IWMProfileManager2**          | \_IWMPROFILEMANAGER2 IID          | 7a924e51-73c1-494d-8019-23d37ed9b89a |
| **IWMProfileManagerLanguage**   | \_IWMPROFILEMANAGERLANGUAGE IID   | ba4dcc78-7ee0-4ab8-b27a-dbce8bc51454 |
| **IWMPropertyVault**            | \_IWMPROPERTYVAULT IID            | 72995A79-5090-42a4-9C8C-D9D0B6D34BE5 |
| **IWMProximityDetection**       | \_IWMPROXIMITYDETECTION IID       | 6A9FD8EE-B651-4bf0-B849-7D4ECE79A2B1 |
| **IWMReader**                   | \_IWMREADER IID                   | 96406bd6-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderAccelerator**        | \_IWMREADERACCELERATOR IID        | BDDC4D08-944D-4D52-A612-46C3FDA07DD4 |
| **IWMReaderAdvanced**           | \_IWMREADERADVANCED IID           | 96406bea-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderAdvanced2**          | \_IWMREADERADVANCED2 IID          | ae14a945-b90c-4d0d-9127-80d665f7d73e |
| **IWMReaderAdvanced3**          | \_IWMREADERADVANCED3 IID          | 5dc0674b-f04b-4a4e-9f2a-b1afde2c8100 |
| **IWMReaderAdvanced4**          | \_IWMREADERADVANCED4 IID          | 945a76a2-12ae-4d48-bd3c-cd1d90399b85 |
| **IWMReaderAdvanced5**          | \_IWMREADERADVANCED5 IID          | 24c44db0-55d1-49ae-a5cc-f13815e36363 |
| **IWMReaderAdvanced6**          | \_IWMREADERADVANCED6 IID          | 18a2e7f8-428f-4acd-8a00-e64639bc93de |
| **IWMReaderAllocatorEx**        | \_IWMREADERALLOCATOREX IID        | 9f762fa7-a22e-428d-93c9-ac82f3aafe5a |
| **IWMReaderCallback**           | \_IWMREADERCALLBACK IID           | 96406bd8-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderCallbackAdvanced**   | \_IWMREADERCALLBACKADVANCED IID   | 96406beb-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderNetworkConfig**      | \_IWMREADERNETWORKCONFIG IID      | 96406bec-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderNetworkConfig2**     | \_IWMREADERNETWORKCONFIG2 IID     | d979a853-042B-4050-8387-c939db22013f |
| **IWMReaderPlaylistBurn**       | \_IWMREADERPLAYLISTBURN IID       | f28c0300-9baa-4477-A846-1744d9cbf533 |
| **IWMReaderStreamClock**        | \_IWMREADERSTREAMCLOCK IID        | 96406bed-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderTimecode**           | \_IWMREADERTIMECODE IID           | F369E2F0-E081-4FE6-8450-B810B2F410D1 |
| **IWMReaderTypeNegotiation**    | \_IWMREADERTYPENEGOTIATION IID    | fdbe5592-81a1-41ea-93bd-735cad1adc5? |
| **IWMRegisterCallback**         | \_IWMREGISTERCALLBACK IID         | cf4b1f99-4de2-4e49-a363-252740d99bc1 |
| **IWMRegisteredDevice**         | \_IWMREGISTEREDDEVICE IID         | a4503bec-5508-4148-97ac-bfa75760a70d |
| **IWMSBufferAllocator**         | \_IWMSBUFFERALLOCATOR IID         | 61103CA4-2033-11d2-9EF1-006097D2D7CF |
| **IWMSInternalAdminNetSource**  | \_IWMSINTERNALADMINNETSOURCE IID  | 8BB23E5F-D127-4afb-8D02-AE5B66D54C78 |
| **IWMSInternalAdminNetSource2** | \_IWMSINTERNALADMINNETSOURCE2 IID | E74D58C3-CF77-4b51-AF17-744687C43EAE |
| **IWMSInternalAdminNetSource3** | \_IWMSINTERNALADMINNETSOURCE3 IID | 6b63d08e-4590-44af-9eb3-57ff1e73bf80 |
| **IWMStatusCallback**           | \_IWMSTATUSCALLBACK IID           | 6d7cdc70-9888-11d3-8edc-00c04f6109cf |
| **IWMStreamConfig**             | \_IWMSTREAMCONFIG IID             | 96406bdc-2b2b-11d3-b36b-00c04f6108ff |
| **IWMStreamConfig2**            | \_IWMSTREAMCONFIG2 IID            | 7688d8cb-fc0d-43bd-9459-5a8dec200cfa |
| **IWMStreamConfig3**            | \_IWMSTREAMCONFIG3 IID            | cb164104-3aa9-45a7-9ac9-4daee131d6e1 |
| **IWMStreamList**               | \_IWMSTREAMLIST IID               | 96406bdd-2b2b-11d3-b36b-00c04f6108ff |
| **IWMStreamPrioritization**     | \_IWMSTREAMPRIORITIZATION IID     | 8c1c6090-f9a8-4748-8ec3-dd1108ba1e77 |
| **IWMSyncReader**               | \_IWMSYNCREADER IID               | 9397f121-7705-4dc9-b049-98b698188414 |
| **IWMSyncReader2**              | \_IWMSYNCREADER2 IID              | faed3d21-1b6b-4af7-8cb6-3e189bbc187b |
| **IWMVideoMediaProps**          | \_IWMVIDEOMEDIAPROPS IID          | 96406bcf-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWatermarkInfo**            | \_IWMWATERMARKINFO IID            | 6F497062-F2E2-4624-8EA7-9DD40D81FC8D |
| **IWMWriter**                   | \_IWMWRITER IID                   | 96406bd4-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWriterAdvanced**           | \_IWMWRITERADVANCED IID           | 96406be3-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWriterAdvanced2**          | \_IWMWRITERADVANCED2 IID          | 962dc1ec-c046-4db8-9cc7-26ceae500817 |
| **IWMWriterAdvanced3**          | \_IWMWRITERADVANCED3 IID          | 2cd6492d-7c37-4e76-9d3b-59261183a22e |
| **IWMWriterFileSink**           | \_IWMWRITERFILESINK IID           | 96406be5-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWriterFileSink2**          | \_IWMWRITERFILESINK2 IID          | 14282ba7-4aef-4205-8ce5-c229035a05bc |
| **IWMWriterFileSink3**          | \_IWMWRITERFILESINK3 IID          | 3fea4feb-2945-47a7-a1dd-c53a8fc4c45c |
| **IWMWriterFileSinkDataUnit**   | \_IWMWRITERFILESINKDATAUNIT IID   | 633392f0-be5c-486b-a09c-10669c7a6c27 |
| **IWMWriterNetworkSink**        | \_IWMWRITERNETWORKSINK IID        | 96406be7-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWriterPostView**           | \_IWMWRITERPOSTVIEW IID           | 81e20ce4-75ef-491a-8004-fc53c45bdc3e |
| **IWMWriterPostViewCallback**   | \_IWMWRITERPOSTVIEWCALLBACK IID   | d9d6549d-a193-4f24-b308-03123d9b7f8d |
| **IWMWriterPreprocess**         | \_IWMWRITERPREPROCESS IID         | fc54a285-38c4-45b5-aa23-85b9f7cb424b |
| **IWMWriterPushSink**           | \_IWMWRITERPUSHSINK IID           | DC10E6A5-072C-467D-BF57-6330A9DDE12A |
| **IWMWriterSink**               | \_IWMWRITERSINK IID               | 96406be4-2b2b-11d3-b36b-00c04f6108ff |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Valori GUID**](guid-values.md)
</dt> </dl>

 

 




