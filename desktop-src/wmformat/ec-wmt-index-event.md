---
title: EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)
description: '\_evento di \_ indice \_ WMT EC'
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Windows Media Format SDK, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Formato Advanced Systems (ASF), EC_WMT_INDEX_EVENT
- ASF (formato avanzato dei sistemi), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047691"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a>EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)

Inviato da Windows Media Format SDK quando un'applicazione usa il writer ASF per indicizzare i file Windows Media Video.

Parametri

*lParam1*

Può essere uno qualsiasi dei seguenti messaggi **di \_ stato di WMT** .



| Message              | Descrizione                                     |
|----------------------|-------------------------------------------------|
| WMT \_ avviato         | L'indicizzazione è iniziata. *lParam2* è zero.          |
| WMT \_ chiuso          | L'indicizzazione è stata completata. *lParam2* è zero. |
| \_stato dell'indice WMT \_ | L'indicizzazione è in corso.                        |



 

*lParam2*

Se *lParam1* è WMT \_ Closed o WMT \_ Started, *lParam2* è zero. Se *lParam1* è \_ lo stato di avanzamento dell'indice WMT \_ , *lParam2* è un **DWORD** che esprime la quantità di avanzamento come percentuale delle dimensioni totali del download.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento su DirectShow QASF**](directshow-qasf-reference.md)
</dt> </dl>

 

 




