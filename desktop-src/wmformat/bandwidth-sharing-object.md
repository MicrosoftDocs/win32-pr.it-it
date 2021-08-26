---
title: Oggetto di condivisione della larghezza di banda
description: Oggetto di condivisione della larghezza di banda
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows MEDIA Format SDK, oggetti di condivisione della larghezza di banda
- Advanced Systems Format (ASF), oggetti di condivisione della larghezza di banda
- ASF (Advanced Systems Format), oggetti di condivisione della larghezza di banda
- oggetti, oggetti di condivisione della larghezza di banda
- condivisione della larghezza di banda, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 449a1e43a8f5c7212f1e9c4240d85eb11c9ee39209fab4313b373a56d017b2dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055601"
---
# <a name="bandwidth-sharing-object"></a>Oggetto di condivisione della larghezza di banda

Un oggetto di condivisione della larghezza di banda viene usato per indicare che due o più flussi, indipendentemente dalle singole velocità in bit, non useranno mai più di una quantità specificata di larghezza di banda tra di essi. Si tratta di un oggetto puramente informativo. Le velocità in bit impostate al suo interno non vengono applicate a livello di codice da alcun oggetto di questo SDK.

Le informazioni sulla condivisione della larghezza di banda sono una parte facoltativa di un profilo. Gli oggetti di condivisione della larghezza di banda possono essere creati per le informazioni di condivisione della larghezza di banda esistenti in un profilo o possono essere creati vuoti, pronti per ricevere nuovi dati. Gli oggetti di condivisione della larghezza di banda non possono esistere indipendentemente da un oggetto profilo. Per salvare il contenuto di un oggetto di condivisione della larghezza di banda, è necessario chiamare [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).

Per creare un oggetto di condivisione della larghezza di banda, chiamare uno dei metodi seguenti.



| Metodo                                                                                  | Descrizione                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | Crea un oggetto di condivisione della larghezza di banda senza dati.                                                                                                           |
| [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | Crea un oggetto di condivisione della larghezza di banda popolato con i dati di un profilo. Usa l'indice di condivisione della larghezza di banda per identificare le informazioni di condivisione della larghezza di banda desiderate. |



 

Entrambi i metodi nella tabella precedente impostano un puntatore a **un'interfaccia IWMBandwidthSharing.** **L'interfaccia IWMStreamList** viene ereditata da **IWMBandwidthSharing,** quindi non è necessario chiamare **QueryInterface** con questo oggetto.

Le interfacce seguenti sono supportate da ogni oggetto di condivisione della larghezza di banda.



| Interfaccia                                          | Descrizione                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | Gestisce le proprietà di un gruppo di flussi che condivideranno la larghezza di banda. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Gestisce l'elenco di flussi che condivideranno la larghezza di banda.                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Condivisione della larghezza di banda**](bandwidth-sharing.md)
</dt> <dt>

[**Oggetto Gestione profili**](profile-manager-object.md)
</dt> <dt>

[**Oggetto Profile**](profile-object.md)
</dt> </dl>

 

 




