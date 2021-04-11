---
title: Utilizzo di tipi di esclusione reciproca personalizzati
description: Utilizzo di tipi di esclusione reciproca personalizzati
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- esclusione reciproca, interfaccia IWMMutualExclusion
- esclusione reciproca, tipi personalizzati
- profili, tipi di esclusione reciproca personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117371"
---
# <a name="using-custom-mutual-exclusion-types"></a>Utilizzo di tipi di esclusione reciproca personalizzati

È possibile utilizzare gli oggetti di esclusione reciproca in un profilo per soddisfare le esigenze di scenari personalizzati. Passando il valore GUID CLSID \_ WMMUTEX \_ Unknown a [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), si informa l'oggetto di esclusione reciproca che si sta usando uno scenario personalizzato.

È necessario controllare manualmente la selezione del flusso quando si legge un file con un valore di esclusione reciproca personalizzato. L'oggetto Reader utilizzerà il primo flusso aggiunto all'esclusione reciproca come valore predefinito.

Usare la procedura seguente per creare un oggetto di esclusione reciproca personalizzata e aggiungerlo a un profilo:

1.  Creare una gestione profili chiamando la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  È possibile iniziare con un profilo esistente o crearne uno completamente nuovo.
    -   Se si usa un profilo esistente, chiamare uno dei metodi Load dell'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Quindi andare al passaggio 4.
    -   Se si sta creando un profilo completamente nuovo, chiamare [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).
3.  Aggiungere i flussi al nuovo profilo chiamando [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream). Configurare i flussi in base alle esigenze usando i metodi di [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig). È anche possibile chiamare **QueryInterface** per accedere ad altre interfacce nell'oggetto di configurazione del flusso.

    **CreateNewStream** crea solo un oggetto di configurazione del flusso e non influisce sul profilo. Dopo aver configurato correttamente un flusso, è necessario chiamare [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) per aggiungere il flusso al profilo.

4.  Creare un oggetto di esclusione reciproca chiamando [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).
5.  Aggiungere i flussi desiderati all'oggetto di esclusione reciproca chiamando [**IWMStreamList:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponibile direttamente da [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), che eredita da [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).
6.  Impostare il tipo di esclusione reciproca su Custom chiamando [**IWMMutualExclusion:: seTYPE**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype). Passare il CLSID \_ WMMUTEX \_ sconosciuto come GUID del tipo.
7.  Aggiungere l'oggetto di esclusione reciproca configurato al profilo chiamando [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interfaccia IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interfaccia IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Interfaccia IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Interfaccia IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Uso dell'esclusione reciproca**](using-mutual-exclusion.md)
</dt> <dt>

[**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




