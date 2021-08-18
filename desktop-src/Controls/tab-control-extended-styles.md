---
title: Stili estesi del controllo Tab (CommCtrl.h)
description: Il controllo Struttura a schede supporta ora gli stili estesi. Questi stili vengono manipolati usando i messaggi TCM \_ GETEXTENDEDSTYLE e TCM SETEXTENDEDSTYLE e non devono essere confusi con gli stili di finestra estesi passati a \_ CreateWindowEx.
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
ms.openlocfilehash: bd057a1ced7c2f594b9e4a7a2c67abe963caa270e770eebecd2f36b50f309aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769921"
---
# <a name="tab-control-extended-styles"></a>Stili estesi del controllo Struttura a schede

Il controllo Struttura a schede supporta ora gli stili estesi. Questi stili vengono manipolati usando i messaggi [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) e [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) e non devono essere confusi con gli stili di finestra estesi passati a [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)



| Costante                                                                                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TCS \_ EX \_ FLATSEPARATORS**</dt> </dl> | [Versione 4.71.](common-control-versions.md) Il controllo Struttura a schede disegna separatori tra gli elementi della scheda. Questo stile esteso influisce solo sui controlli struttura a schede con gli stili [**\_ TCS BUTTONS**](tab-control-styles.md) [**e \_ FLATBUTTONS di TCS.**](tab-control-styles.md) Per impostazione predefinita, la creazione del controllo struttura a schede con lo stile **\_ FLATBUTTONS di TCS** imposta questo stile esteso. Se non sono necessari separatori, è necessario rimuovere questo stile esteso dopo aver creato il controllo.<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TCS \_ EX \_ REGISTERDROP**</dt> </dl>       | [Versione 4.71.](common-control-versions.md) Il controllo Struttura a schede genera codici di notifica [ \_ TCN GETOBJECT](tcn-getobject.md) per richiedere un oggetto destinazione di rilascio quando un oggetto viene trascinato sugli elementi della scheda nel controllo. L'applicazione deve chiamare [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) prima di impostare questo stile. <br/>                                                                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

