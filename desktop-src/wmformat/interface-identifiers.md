---
title: Identificatori di interfaccia
description: Identificatori di interfaccia
ms.assetid: 009edcc0-34db-40a1-ae76-17492b11604a
keywords:
- Windows MEDIA Format SDK, identificatori di interfaccia (IID)
- Advanced Systems Format (ASF), identificatori di interfaccia (IID)
- ASF (Advanced Systems Format),identificatori di interfaccia (IID)
- identificatori di interfaccia (IID)
- IID (identificatori di interfaccia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d32dc097e251c7fd82ff3b7ae5320d6bc1bfc628d32d436256a8a5c15bd7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808921"
---
# <a name="interface-identifiers"></a>Identificatori di interfaccia

È necessario usare un identificatore di interfaccia (IID) quando si effettuano chiamate al **metodo QueryInterface.** Un IID è un valore guid (Globally Unique Identifier). Nell'SDK Windows Media Format la costante assegnata all'IID per una determinata interfaccia è il nome dell'interfaccia preceduto da \_ 'IID'.

Nella tabella seguente sono elencati gli identificatori di interfaccia e le costanti associate per le interfacce in questo SDK.



| Interfaccia                       | Costante IID                     | GUID                                 |
|---------------------------------|----------------------------------|--------------------------------------|
| **INSSBuffer**                  | IID \_ INSSBuffer                  | E1CD3524-03D7-11d2-9EED-006097D2D7CF |
| **INSSBuffer2**                 | IID \_ INSSBuffer2                 | 4f528693-1035-43fe-b428-757561ad3a68 |
| **INSSBuffer3**                 | IID \_ INSSBuffer3                 | c87ceaaf-75be-4bc4-84eb-ac2798507672 |
| **INSSBuffer4**                 | IID \_ INSSBuffer4                 | b6b8fd5a-32e2-49d4-a910-c26cc85465ed |
| **IWMAddressAccess**            | IID \_ IWMAddressAccess            | BB3C6389-1633-4E92-AF14-9F3173BA39D0 |
| **IWMAddressAccess2**           | IID \_ IWMAddressAccess2           | 65A83FC2-3E98-4D4D-81B5-2A742886B33D |
| **IWMBackupRestoreProps**       | IID \_ IWMBackupRestoreProps       | 3C8E0DA6-996F-4ff3-A1AF-4838F9377e2e |
| **IWMBandwidthSharing**         | IID \_ IWMBandwidthSharing         | ad694af1-f8d9-42f8-bc47-70311b0c4f9e |
| **IWMClientConnections**        | IID \_ IWMClientConnections        | 73c66010-a299-41df-b1f0-ccf03b09c1c6 |
| **IWMClientConnections2**       | IID \_ IWMClientConnections2       | 4091571e-4701-4593-bb3d-d5f5f0c74246 |
| **IWMCodecInfo**                | IID \_ IWMCodecInfo                | a970f41e-34de-4a98-b3ba-e4b3ca7528f0 |
| **IWMCodecInfo2**               | IID \_ IWMCodecInfo2               | aa65e273-b686-4056-91ec-dd768d4df710 |
| **IWMCodecInfo3**               | IID \_ IWMCodecInfo3               | 7e51f487-4d93-4f98-8ab4-27d0565adc51 |
| **IWMCredentialCallback**       | IID \_ IWMCredentialCallback       | 342e0eb7-e651-450c-975b-2ace2c90c48e |
| **IWMDeviceRegistration**       | IID \_ IWMDeviceRegistration       | f6211f03-8d21-4e94-93e6-8510805f2d99 |
| **IWMDRMEditor**                | IID \_ IWMDRMEditor                | FF130EBC-A6C3-42A6-B401-C3382C3E08B3 |
| **IWMDRMMessageParser**         | IID \_ IWMDRMMessageParser         | a73a0072-25a0-4c99-b4a5-ede8101a6c39 |
| **IWMDRMReader**                | IID \_ IWMDRMReader                | d2827540-3ee7-432c-b14c-dc17f085d3b3 |
| **IWMDRMReader2**               | IID \_ IWMDRMReader2               | befe7a75-9f1d-4075-b9d9-a3c37bda49a0 |
| **IWMDRMReader3**               | IID \_ IWMDRMReader3               | f28c0300-9baa-4477-a846-1744d9cbf533 |
| **IWMDRMTranscryptor**          | IID \_ IWMDRMTranscryptor          | 69059850-6e6f-4bb2-806f-71863ddfc471 |
| **IWMDRMWriter**                | IID \_ IWMDRMWriter                | D6EA5DD0-12A0-43F4-90AB-A3FD451E6A07 |
| **IWMDRMWriter2**               | IID \_ IWMDRMWriter2               | 38ee7a94-40e2-4e10-aa3f-33fd3210ed5b |
| **IWMDRMWriter3**               | IID \_ IWMDRMWriter3               | a7184082-a4aa-4dde-ac9c-e75dbd1117ce |
| **IWMHeaderInfo**               | IID \_ IWMHeaderInfo               | 96406bda-2b2b-11d3-b36b-00c04f6108ff |
| **IWMHeaderInfo2**              | IID \_ IWMHeaderInfo2              | 15cf9781-454e-482e-b393-85fae487a810 |
| **IWMHeaderInfo3**              | IID \_ IWMHeaderInfo3              | 15CC68E3-27CC-4ecd-B222-3F5D02D80BD5 |
| **IWMImageInfo**                | IID \_ IWMImageInfo                | 9F0AA3B6-7267-4D89-88F2-BA915AA5C4C6 |
| **IWMIndexer**                  | IID \_ IWMIndexer                  | 6d7cdc71-9888-11d3-8edc-00c04f6109cf |
| **IWMIndexer2**                 | IID \_ IWMIndexer2                 | b70f1e42-6255-4df0-a6b9-02b212d9e2bb |
| **IWMInputMediaProps**          | IID \_ IWMInputMediaProps          | 96406bd5-2b2b-11d3-b36b-00c04f6108ff |
| **IWMIStreamProps**             | IID \_ IWMIStreamProps             | 6816dad3-2b4b-4c8e-8149-874c3483a753 |
| **IWMLanguageList**             | IID \_ IWMLanguageList             | DF683F00-2D49-4D8E-92B7-FB19F6A0DC57 |
| **IWMLicenseBackup**            | IID \_ IWMLicenseBackup            | 05E5AC9F-3FB6-4508-BB43-A4067BA1EBE8 |
| **IWMLicenseRestore**           | IID \_ IWMLicenseRestore           | C70B6334-a22e-4efb-A245-15E65A004A13 |
| **IWMLicenseRevocationAgent**   | \_IWMLicenseRevocationAgent IWMLicense   | 6967f2c9-4e26-4b57-8894-799880f7ac7b |
| **IWMMediaProps**               | IID \_ IWMMediaProps               | 96406bce-2b2b-11d3-b36b-00c04f6108ff |
| **IWMMetadataEditor**           | IID \_ IWMMetadataEditor           | 96406bd9-2b2b-11d3-b36b-00c04f6108ff |
| **IWMMetadataEditor2**          | IID \_ IWMMetadataEditor2          | 203cffe3-2e18-4fdf-b59d-6e71530534cf |
| **IWMMutualExclusion**          | IID \_ IWMMutualExclusion          | 96406bde-2b2b-11d3-b36b-00c04f6108ff |
| **IWMMutualExclusion2**         | IID \_ IWMMutualExclusion2         | 302b57d?-89d1-4ba2-85c9-166f2c53eb91 |
| **IWMOutputMediaProps**         | IID \_ IWMOutputMediaProps         | 96406bd7-2b2b-11d3-b36b-00c04f6108ff |
| **IWMPacketSize**               | IID \_ IWMPacketSize               | cdfb97ab-188f-40b3-b643-5b7903975c59 |
| **IWMPacketSize2**              | IID \_ IWMPacketSize2              | 8bfc2b9e-b646-4233-a877-1c6a7?9669dc |
| **IWMPlayerHook**               | IID \_ IWMPlayerHook               | e5b7ca9a-0f1c-4f66-9002-74ec50d8b304 |
| **Profilo IWM**                  | IID \_ IWMProfile                  | 96406bdb-2b2b-11d3-b36b-00c04f6108ff |
| **IWMProfile2**                 | IID \_ IWMProfile2                 | 07e72d33-d94e-4be7-8843-60ae5ff7e5f5 |
| **IWMProfile3**                 | IID \_ IWMProfile3                 | 00ef96cc-a461-4546-8bcd-c9a28f0e06f5 |
| **IWMProfileManager**           | IID \_ IWMProfileManager           | d16679f2-6ca0-472d-8d31-2f5d55aee155 |
| **IWMProfileManager2**          | IID \_ IWMProfileManager2          | 7a924e51-73c1-494d-8019-23d37ed9b89a |
| **IWMProfileManagerLanguage**   | IID \_ IWMProfileManagerLanguage   | ba4dcc78-7ee0-4ab8-b27a-dbce8bc51454 |
| **IWMPropertyVault**            | IID \_ IWMPropertyVault            | 72995A79-5090-42a4-9C8C-D9D0B6D34BE5 |
| **IWMProximityDetection**       | \_IWMProximityDetection IWM       | 6A9FD8EE-B651-4bf0-B849-7D4ECE79A2B1 |
| **IWMReader**                   | IID \_ IWMReader                   | 96406bd6-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderAccelerator**        | IID \_ IWMReaderAccelerator        | BDDC4D08-944D-4D52-A612-46C3FDA07DD4 |
| **IWMReaderAdvanced**           | IID \_ IWMReaderAdvanced           | 96406bea-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderAdvanced2**          | IID \_ IWMReaderAdvanced2          | ae14a945-b90c-4d0d-9127-80d665f7d73e |
| **IWMReaderAdvanced3**          | IID \_ IWMReaderAdvanced3          | 5dc0674b-f04b-4a4e-9f2a-b1afde2c8100 |
| **IWMReaderAdvanced4**          | IID \_ IWMReaderAdvanced4          | 945a76a2-12ae-4d48-bd3c-cd1d90399b85 |
| **IWMReaderAdvanced5**          | IID \_ IWMReaderAdvanced5          | 24c44db0-55d1-49ae-a5cc-f13815e36363 |
| **IWMReaderAdvanced6**          | IID \_ IWMReaderAdvanced6          | 18a2e7f8-428f-4acd-8a00-e64639bc93de |
| **IWMReaderAllocatorEx**        | IID \_ IWMReaderAllocatorEx        | 9f762fa7-a22e-428d-93c9-ac82f3aafe5a |
| **IWMReaderCallback**           | IID \_ IWMReaderCallback           | 96406bd8-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderCallbackAdvanced**   | IID \_ IWMReaderCallbackAdvanced   | 96406beb-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderNetworkConfig**      | IID \_ IWMReaderNetworkConfig      | 96406bec-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderNetworkConfig2**     | IID \_ IWMReaderNetworkConfig2     | d979a853-042b-4050-8387-c939db22013f |
| **IWMReaderPlaylist Rielenco**       | IID \_ IWMReaderPlaylist Rielenco       | f28c0300-9baa-4477-a846-1744d9cbf533 |
| **IWMReaderStreamClock**        | IID \_ IWMReaderStreamClock        | 96406bed-2b2b-11d3-b36b-00c04f6108ff |
| **IWMReaderTimecode**           | IID \_ IWMReaderTimecode           | F369E2F0-E081-4FE6-8450-B810B2F410D1 |
| **IWMReaderTypeNegotiation**    | IID \_ IWMReaderTypeNegotiation    | fdbe5592-81a1-41ea-93bd-735cad1adc5? |
| **IWMRegisterCallback**         | IID \_ IWMRegisterCallback         | cf4b1f99-4de2-4e49-a363-252740d99bc1 |
| **IWMRegisteredDevice**         | IID \_ IWMRegisteredDevice         | a4503bec-5508-4148-97ac-bfa75760a70d |
| **IWMSBufferAllocator**         | IID \_ IWMSBufferAllocator         | 61103CA4-2033-11d2-9EF1-006097D2D7CF |
| **IWMSInternalAdminNetSource**  | IID \_ IWMSInternalAdminNetSource  | 8BB23E5F-D127-4afb-8D02-AE5B66D54C78 |
| **IWMSInternalAdminNetSource2** | IID \_ IWMSInternalAdminNetSource2 | E74D58C3-CF77-4b51-AF17-744687C43EAE |
| **IWMSInternalAdminNetSource3** | IID \_ IWMSInternalAdminNetSource3 | 6b63d08e-4590-44af-9eb3-57ff1e73bf80 |
| **IWMStatusCallback**           | IID \_ IWMStatusCallback           | 6d7cdc70-9888-11d3-8edc-00c04f6109cf |
| **IWMStreamConfig**             | IID \_ IWMStreamConfig             | 96406bdc-2b2b-11d3-b36b-00c04f6108ff |
| **IWMStreamConfig2**            | IID \_ IWMStreamConfig2            | 7688d8cb-fc0d-43bd-9459-5a8dec200cfa |
| **IWMStreamConfig3**            | IID \_ IWMStreamConfig3            | cb164104-3aa9-45a7-9ac9-4daee131d6e1 |
| **IWMStreamList**               | IID \_ IWMStreamList               | 96406bdd-2b2b-11d3-b36b-00c04f6108ff |
| **IWMStreamPrioritization**     | IID \_ IWMStreamPrioritization     | 8c1c6090-f9a8-4748-8ec3-dd1108ba1e77 |
| **IWMSyncReader**               | IID \_ IWMSyncReader               | 9397f121-7705-4dc9-b049-98b698188414 |
| **IWMSyncReader2**              | IID \_ IWMSyncReader2              | faed3d21-1b6b-4af7-8cb6-3e189bbc187b |
| **IWMVideoMediaProps**          | IID \_ IWMVideoMediaProps          | 96406bcf-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWatermarkInfo**            | IID \_ IWMWatermarkInfo            | 6F497062-F2E2-4624-8EA7-9DD40D81FC8D |
| **IWMWriter**                   | IID \_ IWMWriter                   | 96406bd4-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWriterAdvanced**           | IID \_ IWMWriterAdvanced           | 96406be3-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWriterAdvanced2**          | IID \_ IWMWriterAdvanced2          | 962dc1ec-c046-4db8-9cc7-26ceae500817 |
| **IWMWriterAdvanced3**          | IID \_ IWMWriterAdvanced3          | 2cd6492d-7c37-4e76-9d3b-59261183a22e |
| **IWMWriterFileSink**           | IID \_ IWMWriterFileSink           | 96406be5-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWriterFileSink2**          | IID \_ IWMWriterFileSink2          | 14282ba7-4aef-4205-8ce5-c229035a05bc |
| **IWMWriterFileSink3**          | IID \_ IWMWriterFileSink3          | 3fea4feb-2945-47a7-a1dd-c53a8fc4c45c |
| **IWMWriterFileSinkDataUnit**   | IID \_ IWMWriterFileSinkDataUnit   | 633392f0-be5c-486b-a09c-10669c7a6c27 |
| **IWMWriterNetworkSink**        | IID \_ IWMWriterNetworkSink        | 96406be7-2b2b-11d3-b36b-00c04f6108ff |
| **IWMWriterPostView**           | IID \_ IWMWriterPostView           | 81e20ce4-75ef-491a-8004-fc53c45bdc3e |
| **IWMWriterPostViewCallback**   | IID \_ IWMWriterPostViewCallback   | d9d6549d-a193-4f24-b308-03123d9b7f8d |
| **IWMWriterPreprocess**         | IID \_ IWMWriterPreprocess         | fc54a285-38c4-45b5-aa23-85b9f7cb424b |
| **IWMWriterPushSink**           | IID \_ IWMWriterPushSink           | DC10E6A5-072C-467D-BF57-6330A9DDE12A |
| **IWMWriterSink**               | IID \_ IWMWriterSink               | 96406be4-2b2b-11d3-b36b-00c04f6108ff |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Valori GUID**](guid-values.md)
</dt> </dl>

 

 




