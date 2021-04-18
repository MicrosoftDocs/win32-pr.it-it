---
title: Stili della descrizione comando (CommCtrl. h)
description: Questa sezione elenca gli stili di controllo usati con i controlli ToolTip.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326842"
---
# <a name="tooltip-styles"></a>Stili descrizione comando

Questa sezione elenca gli stili di controllo usati con i controlli ToolTip.



| Costante                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**\_ALWAYSTIP TTS**</dt> </dl>                | Indica che il controllo ToolTip viene visualizzato quando il cursore si trova in uno strumento, anche se la finestra proprietaria del controllo ToolTip è inattiva. Senza questo stile, la descrizione comando viene visualizzata solo quando la finestra proprietaria dello strumento è attiva.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**\_fumetto TTS**</dt> </dl>                      | [Versione 5,80](common-control-versions.md). Indica che il controllo ToolTip ha l'aspetto di un fumetto "Balloon", con angoli arrotondati e un gambo che punta all'elemento. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**TTS \_ chiuso**</dt> </dl>                            | Visualizza un pulsante **Chiudi** nella descrizione comando. Valido solo quando la descrizione comando ha lo \_ stile e un titolo del fumetto TTS; vedere [**\_ TTM**](ttm-settitle.md).<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**TTS \_ NOanimate**</dt> </dl>                | [Versione 5,80](common-control-versions.md). Disabilita l'animazione scorrevole della descrizione comando nei sistemi Windows 98 e Windows 2000. Questo stile viene ignorato nei sistemi precedenti.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS \_ NOfade**</dt> </dl>                         | [Versione 5,80](common-control-versions.md). Disabilita l'animazione della descrizione comando dissolvenza. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**\_prefisso TTS**</dt> </dl>                   | Impedisce al sistema di estrarre i caratteri e commerciale da una stringa o di terminare una stringa in corrispondenza di un carattere di tabulazione. Senza questo stile, il sistema rimuove automaticamente i caratteri e e termina una stringa in corrispondenza del primo carattere di tabulazione. Questo consente a un'applicazione di usare la stessa stringa sia come voce di menu che come testo in un controllo ToolTip.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**\_USEVISUALSTYLE TTS**</dt> </dl> | Usa collegamenti ipertestuali con tema. Il tema definisce gli stili per tutti i collegamenti nella descrizione comando. Per questo stile è sempre necessario \_ impostare ttf PARSELINKS. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

Un controllo ToolTip presenta sempre gli \_ stili della finestra WS popup e WS \_ ex \_ TOOLWINDOW, indipendentemente dal fatto che vengano specificati quando si crea il controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





