---
title: Per caricare un profilo di sistema
description: Per caricare un profilo di sistema
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- profili, sistema
- profili di sistema, caricamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398581"
---
# <a name="to-load-a-system-profile"></a>Per caricare un profilo di sistema

Per apportare modifiche a un profilo di sistema, è necessario caricarlo in un oggetto profilo. Gestione profili fornisce due opzioni per il caricamento dei profili di sistema: per identificatore e per indice.

Un identificatore del profilo di sistema è un valore GUID assegnato al profilo di sistema al momento della creazione. Per un elenco delle costanti GUID associate ai profili di sistema versione 8, vedere profili di [sistema](system-profiles.md). È possibile trovare le costanti GUID per le versioni precedenti nel file di intestazione WMSysPrf. h. Per ulteriori informazioni su questo e altri file di intestazione inclusi con Windows Media Format SDK, vedere [file di libreria e impostazioni del compilatore](library-files-and-compiler-settings.md).

Nell'esempio di codice seguente viene illustrato come caricare un profilo di sistema utilizzando l'identificatore del profilo di sistema. Per il corretto funzionamento di questo codice, è necessario includere WMSysPrf. h e stdio. h. Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).


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



Se non si conosce il profilo che si vuole usare, è possibile scorrere tutti i profili di sistema di una determinata versione usando i metodi [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) e [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) dell'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Questi metodi gestiscono solo una versione dei profili di sistema alla volta. Per ulteriori informazioni sulla modifica della versione del profilo di sistema, vedere [per modificare le versioni del profilo di sistema](to-change-system-profile-versions.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei profili di sistema**](using-system-profiles.md)
</dt> </dl>

 

 




