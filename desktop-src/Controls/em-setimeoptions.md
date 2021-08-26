---
title: EM_SETIMEOPTIONS messaggio (Richedit.h)
description: Imposta le opzioni IME (Input Method Editor).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ffae9586c3ee05f951672f0927c4f10ad2115684643af8418062bb7724c7b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048391"
---
# <a name="em_setimeoptions-message"></a>Messaggio EM \_ SETIMEOPTIONS

Imposta le opzioni IME (Input Method Editor).

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asia di Microsoft Rich Edit 1.0. Non è supportato nelle versioni successive.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno dei valori seguenti.



| Valore                                                                                                                                             | Significato                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**SET DI \_ ECOOP**</dt> </dl> | Imposta le opzioni su quelle specificate da *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ OR**</dt> </dl>    | Combina le opzioni specificate con le opzioni correnti.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ E**</dt> </dl> | Mantiene solo le opzioni correnti specificate anche da *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | OR esclusivo logicamente le opzioni correnti con quelle specificate da *lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica uno o più dei valori seguenti.



| Valore                                                                                                                                                                                 | Significato                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**IMF \_ CLOSESTATUSWINDOW**</dt> </dl> | Chiude la finestra di stato IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**IMF \_ FORCEACTIVE**</dt> </dl>                   | Attiva l'IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**IMF \_ FORCEDISABLE**</dt> </dl>                | Disabilita l'IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**IMF \_ FORCEENABLE**</dt> </dl>                   | Abilita l'IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**IMF \_ FORCEINACTIVE**</dt> </dl>             | Disattiva l'IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**IMF \_ FORCENONE**</dt> </dl>                         | Disabilita la gestione IME.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**IMF \_ FORCEREMEMBER**</dt> </dl>             | Ripristina lo stato IME precedente quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**IMF \_ MULTIPLEEDIT**</dt> </dl>                | Specifica che la stringa di composizione non verrà annullata o determinata dalle modifiche dello stato attivo. Ciò consente a un'applicazione di avere stringhe di composizione separate in ogni controllo Rich Edit.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**IMF \_ VERTICALE**</dt> </dl>                            | Nota usata in Rich Edit 2.0 e versioni successive. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione non riesce, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)
</dt> </dl>

 

 





