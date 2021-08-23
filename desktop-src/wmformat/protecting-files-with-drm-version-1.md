---
title: Protezione dei file con DRM versione 1
description: Protezione dei file con DRM versione 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Media Format SDK, creazione di file protetti
- Windows Media Format SDK,file protetti
- Advanced Systems Format (ASF), creazione di file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- Advanced Systems Format (ASF), file protetti
- ASF (Advanced Systems Format), file protetti
- Advanced Systems Format (ASF), WMStubDRM.lib
- ASF (Advanced Systems Format),WMStubDRM.lib
- WMStubDRM.lib,creazione di file protetti
- WMStubDRM.lib,file protetti
- digital rights management (DRM), WMStubDRM.lib
- DRM (digital rights management),WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b500f3711b8c92324cbd87d4dc199a8a0bb803cba69357a23f139fb96f8281f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084538"
---
# <a name="protecting-files-with-drm-version-1"></a>Protezione dei file con DRM versione 1

Quando viene applicato questo tipo di protezione, viene generata una licenza DRM versione 1 valida solo nel computer da cui è stata effettuata la richiesta di licenza. Poiché non è impostata alcuna chiave o valore di seeding della chiave, non è possibile generare licenze portabili per il contenuto protetto con questa tecnica. Tuttavia, quando si usa Windows Media Format SDK 7.1 o versione successiva, le licenze sono recuperabili nel servizio Migrazione licenze Microsoft.

Per proteggere i file ASF usando DRM versione 1, seguire questa procedura:

1.  Collegare il file WMStubDRM.lib al progetto e, se necessario, scollegare wmvcore.lib.
2.  Chiamare la [**funzione WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) per creare il writer. Il primo argomento è riservato e deve essere impostato su **NULL.**
3.  Impostare un profilo da usare per il writer chiamando [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). È necessario impostare un profilo nel writer prima di impostare gli attributi DRM. DRM è supportato solo per i profili che usano Windows codec Media Audio o Windows Media Video.
4.  Usando il [**metodo IWMHeaderInfo::SetAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) impostare le proprietà DRM seguenti. La **proprietà \_ Use DRM** indica ai componenti DRM di proteggere il contenuto usando DRM versione 1. La **proprietà \_ Flag DRM** specifica i diritti da includere nella licenza locale che verrà creata per il contenuto. Anche **il valore DRM \_ LEVEL** viene archiviato nella licenza. Specifica il livello minimo necessario per accedere al contenuto. 150 è il livello consigliato per il contenuto DRM versione 1.

    | Attributo      | Valore                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Usare \_ DRM**   | **TRUE**                                                                                    |
    | **Flag \_ DRM** | WMT \_ RIGHT \_ PLAYBACK \| WMT \_ RIGHT \_ COPY \_ TO \_ NON \_ SDMI \_ DEVICE \| WMT \_ RIGHT \_ COPY \_ TO \_ CD |
    | **LIVELLO \_ DRM** | 150                                                                                         |

    

     

Il codice di esempio seguente illustra come creare un writer abilitato per DRM per DRM versione 1 e impostare le proprietà DRM. Il controllo degli errori è stato omesso per chiarire.


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




