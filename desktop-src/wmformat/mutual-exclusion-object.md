---
title: Oggetto di esclusione reciproca
description: Oggetto di esclusione reciproca
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Media Format SDK, oggetti di esclusione reciproca
- Advanced Systems Format (ASF), oggetti di esclusione reciproca
- ASF (Advanced Systems Format), oggetti di esclusione reciproca
- oggetti, oggetti di esclusione reciproca
- esclusione reciproca, oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d7e780ac18dcad7ef04f9bb50d3a7389851156866980b21fbe0c231bcb057d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929931"
---
# <a name="mutual-exclusion-object"></a>Oggetto di esclusione reciproca

Un oggetto di esclusione reciproca viene usato per specificare un numero di flussi, di cui solo uno può essere recapitato alla volta. Può essere usato in diversi modi, ad esempio fornendo un flusso audio in diverse lingue come colonna sonora per un flusso video.

L'esclusione reciproca è una parte facoltativa di un profilo. Gli oggetti di esclusione reciproca possono essere creati per le informazioni di esclusione reciproca esistenti in un profilo o possono essere creati vuoti, pronti per ricevere nuovi dati. Gli oggetti di esclusione reciproca non possono esistere indipendentemente da un oggetto profilo. Per salvare il contenuto di un oggetto di esclusione reciproca, è necessario chiamare [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

Per creare un oggetto di esclusione reciproca, usare uno dei metodi seguenti.



| Metodo                                                                              | Descrizione                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Crea un oggetto di esclusione reciproca senza dati.                                                                                                         |
| [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Crea un oggetto di esclusione reciproca popolato con i dati di un profilo. Usa l'indice di esclusione reciproca per identificare le informazioni di esclusione reciproca desiderate. |



 

Entrambi i metodi nella tabella precedente impostano un puntatore a **un'interfaccia IWMMutualExclusion.** **L'interfaccia IWMStreamList** viene ereditata da **IWMMutualExclusion** e non deve mai essere accessibile direttamente. L'altra interfaccia dell'oggetto di esclusione reciproca può essere ottenuta chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate da ogni oggetto di esclusione reciproca.



| Interfaccia                                          | Descrizione                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | Imposta e recupera il tipo di esclusione reciproca da utilizzare.                                                                                            |
| [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | Organizza i flussi in record, che possono essere usati per creare scenari di esclusione reciproca complessi. Eredita tutti i metodi di **IWMMutualExclusion.** |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Gestisce l'elenco di flussi che si escludono a vicenda.                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esclusione reciproca**](mutual-exclusion.md)
</dt> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Gestione profili**](profile-manager-object.md)
</dt> </dl>

 

 




