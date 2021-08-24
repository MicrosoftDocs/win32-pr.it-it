---
title: Stili della descrizione comando (CommCtrl.h)
description: Questa sezione elenca gli stili dei controlli usati con i controlli descrizione comando.
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
ms.openlocfilehash: 2dddd890f8bf3aad35d20ec2eabcbe34f89b3ef262fbe30586f9a0a893f85e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751024"
---
# <a name="tooltip-styles"></a>Stili della descrizione comando

Questa sezione elenca gli stili dei controlli usati con i controlli descrizione comando.



| Costante                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**TTS \_ ALWAYSTIP**</dt> </dl>                | Indica che il controllo descrizione comando viene visualizzato quando il cursore si trova su uno strumento, anche se la finestra proprietaria del controllo descrizione comando è inattiva. Senza questo stile, la descrizione comando viene visualizzata solo quando la finestra proprietaria dello strumento è attiva.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**TTS \_ BALLOON**</dt> </dl>                      | [Versione 5.80.](common-control-versions.md) Indica che il controllo descrizione comando ha l'aspetto di un "fumetto" con angoli arrotondati e un gambo che punta all'elemento. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**TTS \_ CLOSE**</dt> </dl>                            | Visualizza un **pulsante Chiudi** nella descrizione comando. Valido solo quando la descrizione comando ha lo stile BALLOON TTS \_ e un titolo. Vedere [**TTM \_ SETTITLE**](ttm-settitle.md).<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**TTS \_ NOANIMATE**</dt> </dl>                | [Versione 5.80.](common-control-versions.md) Disabilita l'animazione della descrizione comando scorrevole Windows 98 e Windows 2000. Questo stile viene ignorato nei sistemi precedenti.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS \_ NOFADE**</dt> </dl>                         | [Versione 5.80.](common-control-versions.md) Disabilita l'animazione della descrizione comando in dissolvente. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**TTS \_ NOPREFIX**</dt> </dl>                   | Impedisce al sistema di rimuovere i caratteri e commerciale da una stringa o di terminare una stringa in corrispondenza di un carattere di tabulazione. Senza questo stile, il sistema rimuove automaticamente i caratteri e commerciale e termina una stringa in corrispondenza del primo carattere di tabulazione. In questo modo un'applicazione può usare la stessa stringa sia come voce di menu che come testo in un controllo descrizione comando.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**TTS \_ USEVISUALSTYLE**</dt> </dl> | Usa collegamenti ipertestuali con testo con testo. Il tema definirà gli stili per tutti i collegamenti nella descrizione comando. Questo stile richiede sempre \_ l'impostazione di TTF PARSELINKS. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

Un controllo descrizione comando ha sempre gli stili delle finestre WS POPUP e \_ WS EX TOOLWINDOW, indipendentemente dal fatto che siano stati specificati durante la \_ \_ creazione del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





