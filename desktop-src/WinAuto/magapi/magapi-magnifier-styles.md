---
title: Stili di ingrandimento
description: Questo argomento descrive gli stili usati con il controllo Magnifier.
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
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400641"
---
# <a name="magnifier-styles"></a>Stili di ingrandimento

Questo argomento descrive gli stili usati con il controllo Magnifier. Per creare un controllo Magnifier, usare la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) e specificare la classe WC_MAGNIFIER Window, insieme a una combinazione degli stili di ingrandimento seguenti.

| Requisito | Valore |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Ritaglia l'area della finestra di ingrandimento che racchiude il cursore di sistema. Questo stile consente all'utente di visualizzare il contenuto della schermata dietro la finestra di ingrandimento. |
| MS_INVERTCOLORS 0x0004L | Visualizza il contenuto della schermata ingrandita utilizzando i colori invertiti. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Visualizza il cursore di sistema ingrandito insieme al contenuto della schermata ingrandita. |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Ingrandimento. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Costanti](entry-magapi-constants.md)
