---
title: Creazione di profili
description: Creazione di profili
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media Format SDK, profili
- profili, creazione
- profili, interfaccia IWMProfileManager
- IWMProfileManager, creazione di profili
- profili, funzione WMCreateProfileManager
- WMCreateProfileManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046279"
---
# <a name="creating-profiles"></a>Creazione di profili

In molti casi, è possibile creare un profilo vuoto da configurare in base alle esigenze. In altri casi è più semplice modificare un profilo esistente, ad esempio un profilo di sistema. Per ulteriori informazioni sull'utilizzo dei profili di sistema, vedere [using System Profiles](using-system-profiles.md).

La creazione di un profilo vuoto, pronto per la configurazione, richiede un oggetto gestore profili. Per ottenere l'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) di un oggetto di gestione profilo, chiamare la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .

Per creare un profilo vuoto, chiamare [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile). Quando si crea un profilo vuoto, l'unica cosa specificata è la versione di Windows Media Format SDK con cui è conforme il profilo. A meno che non sia necessario usare una versione precedente, è sempre necessario usare la versione più recente. La versione impone la struttura del profilo; le versioni precedenti non supportavano alcune proprietà.

Nell'esempio di codice seguente viene illustrato come creare un nuovo profilo. Per compilare il codice nell'applicazione, includere STDIO. h. Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interfaccia IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Utilizzo dei profili**](working-with-profiles.md)
</dt> </dl>

 

 




