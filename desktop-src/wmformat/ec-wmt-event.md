---
title: EC_WMT_EVENT (Windows Media Format 11 SDK)
description: EVENTO \_ EC WMT \_
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows Media Format SDK,EC_WMT_EVENT
- DirectShow,EC_WMT_EVENT
- EC_WMT_EVENT
- digital rights management (DRM), EC_WMT_EVENT
- DRM (digital rights management), EC_WMT_EVENT
- Advanced Systems Format (ASF), EC_WMT_EVENT
- ASF (Advanced Systems Format), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe0e53a759515914a352707550e281aca3aebe096f168352c36c1ff4200b2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118029220"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (Windows Media Format 11 SDK)

Inviato dall'SDK Windows Media Format quando un'applicazione usa il filtro lettore ASF per riprodurre file ASF protetti da DRM (Digital Rights Management).

Parametri

*lParam1*

Può essere uno dei valori WMT \_ STATUS seguenti.



| Messaggio DI \_ STATO WMT           | Descrizione                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| NESSUN \_ DIRITTO WMT \_               | Il file è protetto con DRM versione 1 e l'applicazione non ha diritti per eseguire l'azione richiesta.                    |
| LICENZA DI ACQUISIZIONE \_ WMT \_         | Il processo di acquisizione della licenza è stato completato. Ciò non significa necessariamente che una licenza sia stata acquisita correttamente. |
| WMT \_ NO \_ RIGHTS \_ EX           | Il file è protetto con DRM versione 7 e l'applicazione non ha diritti per eseguire l'azione richiesta.                    |
| WMT \_ RICHIEDE \_ L'INDIVIDUALIZZAZIONE | La licenza consente solo alle applicazioni individualizzate di eseguire l'azione richiesta.                                           |
| INDIVIDUALIZZARE \_ WMT            | Il processo di individualizzazione è in corso o è stato completato.                                                    |



 

*lParam2*

Puntatore a una struttura **\_ AM WMT EVENT \_ \_ DATA** che contiene informazioni sull'evento nel puntatore del membro **pData,** nonché un codice di stato **HRESULT** inviato da Windows Media Format SDK. Il valore di *lParam2* dipende dal valore di *lParam1*, come descritto nella tabella seguente. Le strutture \_ "WM" sono definite in Windows Media Format SDK.



| Se lParam1 è ...              | AM \_ WMT \_ EVENT \_ DATA.pData è...                            |
|-------------------------------|-------------------------------------------------------------|
| NESSUN \_ DIRITTO WMT \_               | Puntatore a una **stringa WCHAR** contenente un URL di richiesta. |
| LICENZA DI ACQUISIZIONE \_ WMT \_         | Puntatore a una **struttura WM GET LICENSE \_ \_ \_ DATA.**        |
| WMT \_ NO \_ RIGHTS \_ EX           | Puntatore a una **struttura WM GET LICENSE \_ \_ \_ DATA.**        |
| WMT \_ RICHIEDE \_ L'INDIVIDUALIZZAZIONE | NULL                                                       |
| INDIVIDUALIZZARE \_ WMT            | Puntatore a una **struttura WM \_ INDIVIDUALIZE \_ STATUS.**     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**DirectShow Informazioni di riferimento su QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




