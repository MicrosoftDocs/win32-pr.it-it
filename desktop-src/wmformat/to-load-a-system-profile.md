---
title: Per caricare un profilo di sistema
description: Per caricare un profilo di sistema
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- profili, sistema
- profili di sistema, caricamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becd98903921b81ce1eaf7d2317659c7760bb99c4e55e07efe336719d5d34ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807481"
---
# <a name="to-load-a-system-profile"></a>Per caricare un profilo di sistema

Per apportare modifiche a un profilo di sistema, è necessario caricarlo in un oggetto profilo. Gestione profili offre due opzioni per il caricamento dei profili di sistema: in base all'identificatore e all'indice.

Un identificatore del profilo di sistema è un valore GUID assegnato al profilo di sistema al momento della creazione. Per un elenco delle costanti GUID associate ai profili di sistema versione 8, vedere [Profili di sistema](system-profiles.md). Le costanti GUID per le versioni precedenti sono disponibili nel file di intestazione WMSysPrf.h. Per altre informazioni su questo e altri file di intestazione inclusi in Windows Media Format SDK, vedere File di [libreria e compilatori Impostazioni](library-files-and-compiler-settings.md).

Il codice di esempio seguente illustra come caricare un profilo di sistema usando l'identificatore del profilo di sistema. Per il funzionamento di questo codice, è necessario includere WMSysPrf.h e stdio.h. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice](using-the-code-examples.md).


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



Se non si conosce il profilo da usare, è possibile scorrere tutti i profili di sistema di una determinata versione usando i metodi [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) dell'interfaccia [**IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) Questi metodi si occupano solo di una versione dei profili di sistema alla volta. Per altre informazioni sulla modifica della versione del profilo di sistema, vedere [Per modificare le versioni del profilo di sistema](to-change-system-profile-versions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei profili di sistema**](using-system-profiles.md)
</dt> </dl>

 

 




