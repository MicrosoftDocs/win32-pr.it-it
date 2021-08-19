---
title: Stili di Lente di ingrandimento
description: Questo argomento descrive gli stili usati con il controllo Lente di ingrandimento.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: ef65f736b50210ed52c542375aa340d5bd85ae38265a71858d82e069d830aa62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052579"
---
# <a name="magnifier-styles"></a>Stili di Lente di ingrandimento

Questo argomento descrive gli stili usati con il controllo Lente di ingrandimento. Per creare un controllo lente di ingrandimento, usare la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) e specificare la classe WC_MAGNIFIER window, insieme a una combinazione degli stili di lente di ingrandimento seguenti.

| Requisito | Valore |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Ritaglia l'area della finestra di lente di ingrandimento che circonda il cursore di sistema. Questo stile consente all'utente di visualizzare il contenuto dello schermo dietro la finestra di lente di ingrandimento. |
| MS_INVERTCOLORS 0x0004L | Visualizza il contenuto dello schermo ingrandito usando colori invertiti. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Visualizza il cursore di sistema ingrandito insieme al contenuto dello schermo ingrandito. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ingrandimentotion.h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Costanti](entry-magapi-constants.md)
