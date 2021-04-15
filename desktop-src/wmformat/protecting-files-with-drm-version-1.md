---
title: Protezione dei file con DRM versione 1
description: Protezione dei file con DRM versione 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Media Format SDK, creazione di file protetti
- Windows Media Format SDK, file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Formato Advanced Systems (ASF), WMStubDRM. lib
- ASF (formato avanzato dei sistemi), WMStubDRM. lib
- WMStubDRM. lib, creazione di file protetti
- WMStubDRM. lib, file protetti
- Digital Rights Management (DRM), WMStubDRM. lib
- DRM (Digital Rights Management), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336650"
---
# <a name="protecting-files-with-drm-version-1"></a>Protezione dei file con DRM versione 1

Quando viene applicato questo tipo di protezione, viene generata una licenza DRM versione 1 che è valida solo nel computer da cui è stata effettuata la richiesta di licenza. Poiché non è impostato alcun valore di inizializzazione chiave o chiave, non è possibile generare licenze portabili per il contenuto protetto mediante questa tecnica. Tuttavia, quando si usa Windows Media Format SDK 7,1 o versione successiva, le licenze sono recuperabili dal servizio migrazione licenze Microsoft.

Per proteggere i file ASF usando DRM versione 1, seguire questa procedura:

1.  Collegare il file WMStubDRM. lib al progetto e, se necessario, scollegare wmvcore. lib.
2.  Chiamare la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) per creare il writer. Il primo argomento è riservato e deve essere impostato su **null**.
3.  Impostare un profilo per il writer da utilizzare chiamando [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Prima di impostare gli attributi DRM, è necessario impostare un profilo nel writer. Il DRM è supportato solo per i profili che usano i codec Windows Media Audio o Windows Media Video.
4.  Utilizzando il metodo [**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , impostare le proprietà DRM seguenti. La proprietà **utilizza \_ DRM** indica ai componenti DRM di proteggere il contenuto utilizzando DRM versione 1. La **proprietà \_ flag DRM** specifica i diritti da includere nella licenza locale che verrà creata per il contenuto. Il valore del **\_ livello di DRM** è archiviato anche nella licenza. specifica il livello minimo necessario per accedere al contenuto. 150 è il livello consigliato per il contenuto DRM versione 1.

    | Attributo      | Valore                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **USA \_ DRM**   | **TRUE**                                                                                    |
    | **\_Flag DRM** | WMT \_ right \_ playback \| WMT \_ right \_ copy \_ to \_ non \_ SDMI \_ Device \| WMT \_ right \_ copy \_ to \_ CD |
    | **\_livello DRM** | 150                                                                                         |

    

     

Nell'esempio di codice seguente viene illustrato come creare un writer abilitato per DRM per DRM versione 1 e impostare le proprietà DRM. Il controllo degli errori è stato omesso per chiarire la causa.


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



 

 




