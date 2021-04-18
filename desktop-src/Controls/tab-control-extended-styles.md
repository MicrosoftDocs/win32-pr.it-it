---
title: Stili estesi del controllo Tab (CommCtrl. h)
description: Il controllo struttura a schede supporta ora gli stili estesi. Questi stili vengono modificati usando i messaggi TCM \_ GETEXTENDEDSTYLE e TCM \_ SETEXTENDEDSTYLE e non devono essere confusi con gli stili di finestra estesi passati a CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327599"
---
# <a name="tab-control-extended-styles"></a>Stili estesi del controllo Tab

Il controllo struttura a schede supporta ora gli stili estesi. Questi stili vengono modificati usando i messaggi [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) e [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) e non devono essere confusi con gli stili di finestra estesi passati a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).



| Costante                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TC \_ ex \_ FLATSEPARATORS**</dt> </dl> | [Versione 4,71](common-control-versions.md). Il controllo struttura a schede trarrà separatori tra le voci di scheda. Questo stile esteso interessa solo i controlli struttura a schede con i [**\_ pulsanti TCS**](tab-control-styles.md) e gli stili [**\_ FLATBUTTONS di TCS**](tab-control-styles.md) . Per impostazione predefinita, la creazione del controllo struttura a schede con lo stile **\_ FLATBUTTONS di TCS** imposta questo stile esteso. Se non sono necessari separatori, è necessario rimuovere questo stile esteso dopo aver creato il controllo.<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TC \_ ex \_ REGISTERDROP**</dt> </dl>       | [Versione 4,71](common-control-versions.md). Il controllo struttura a schede genera codici di notifica [ \_ GetObject TCN](tcn-getobject.md) per richiedere un oggetto di destinazione di rilascio quando un oggetto viene trascinato sugli elementi di tabulazione del controllo. Prima di impostare questo stile, l'applicazione deve chiamare [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) . <br/>                                                                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

