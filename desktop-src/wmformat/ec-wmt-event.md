---
title: EC_WMT_EVENT (Windows Media Format 11 SDK)
description: '\_evento WMT \_ EC'
ms.assetid: 51d51659-8e7d-49b7-83f2-a80e99d39d78
keywords:
- Windows Media Format SDK, EC_WMT_EVENT
- DirectShow, EC_WMT_EVENT
- EC_WMT_EVENT
- Digital Rights Management (DRM), EC_WMT_EVENT
- DRM (Digital Rights Management), EC_WMT_EVENT
- Formato Advanced Systems (ASF), EC_WMT_EVENT
- ASF (formato avanzato dei sistemi), EC_WMT_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe74baaba676a97e609b4c03cd4db9010bd8f6a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474855"
---
# <a name="ec_wmt_event-windows-media-format-11-sdk"></a>EC_WMT_EVENT (Windows Media Format 11 SDK)

Inviato da Windows Media Format SDK quando un'applicazione usa il filtro di lettura ASF per riprodurre file ASF protetti da Digital Rights Management (DRM).

Parametri

*lParam1*

Può essere uno dei seguenti valori di \_ stato di WMT.



| \_Messaggio di stato WMT           | Descrizione                                                                                                                    |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| \_nessun \_ diritto di WMT               | Il file è protetto con DRM versione 1 e l'applicazione non ha diritti per eseguire l'azione richiesta.                    |
| \_licenza di acquisizione WMT \_         | Il processo di acquisizione della licenza è stato completato. Questo non significa necessariamente che sia stata acquisita correttamente una licenza. |
| WMT \_ No \_ Rights \_           | Il file è protetto con DRM versione 7 e l'applicazione non ha diritti per eseguire l'azione richiesta.                    |
| WMT \_ richiede l' \_ individualizzazione | La licenza consente solo alle applicazioni individuali di eseguire l'azione richiesta.                                           |
| WMT di \_ personalizzazione            | Il processo di individualizzazione viene ora eseguito o completato.                                                    |



 

*lParam2*

Puntatore a una struttura di **\_ dati dell' \_ evento \_ am WMT** che contiene informazioni sull'evento nel puntatore del membro **pData** , nonché un codice di stato **HRESULT** inviato da Windows Media Format SDK. Il valore di *lParam2* dipende dal valore di *lParam1*, come descritto nella tabella seguente. (Le strutture "WM \_ " sono definite in Windows Media Format SDK).



| Se lParam1 è...              | \_ \_ I dati dell'evento am WMT \_ . pData è...                            |
|-------------------------------|-------------------------------------------------------------|
| \_nessun \_ diritto di WMT               | Puntatore a una stringa **WCHAR** contenente un URL della richiesta di verifica. |
| \_licenza di acquisizione WMT \_         | Puntatore a una struttura **di \_ \_ \_ dati di licenza WM Get** .        |
| WMT \_ No \_ Rights \_           | Puntatore a una struttura **di \_ \_ \_ dati di licenza WM Get** .        |
| WMT \_ richiede l' \_ individualizzazione | NULL                                                       |
| WMT di \_ personalizzazione            | Puntatore a una struttura **di \_ \_ stato di personalizzazione WM** .     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Informazioni di riferimento su DirectShow QASF**](directshow-qasf-reference.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




