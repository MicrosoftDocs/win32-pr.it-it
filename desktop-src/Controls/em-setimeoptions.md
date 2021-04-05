---
title: Messaggio di EM_SETIMEOPTIONS (RichEdit. h)
description: Imposta le opzioni IME (Input Method Editor).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- Controlli di Windows Message EM_SETIMEOPTIONS
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
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874038"
---
# <a name="em_setimeoptions-message"></a>\_Messaggio SETIMEOPTIONS em

Imposta le opzioni IME (Input Method Editor).

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0. Non è supportata nelle versioni successive.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno dei valori seguenti.



| Valore                                                                                                                                             | Significato                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**SET di ECOOP \_**</dt> </dl> | Imposta le opzioni su quelle specificate da *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ o**</dt> </dl>    | Combina le opzioni specificate con le opzioni correnti.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ e**</dt> </dl> | Mantiene solo le opzioni correnti specificate anche da *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**\_Xor ECOOP**</dt> </dl> | Logicamente esclusivo o opzioni correnti con quelle specificate da *lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica uno o più dei valori seguenti.



| Valore                                                                                                                                                                                 | Significato                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**\_CLOSESTATUSWINDOW FMI**</dt> </dl> | Chiude la finestra di stato IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**\_FORCEACTIVE FMI**</dt> </dl>                   | Attiva l'IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**\_FORCEDISABLE FMI**</dt> </dl>                | Disabilita l'IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**\_FORCEENABLE FMI**</dt> </dl>                   | Abilita l'IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**\_FORCEINACTIVE FMI**</dt> </dl>             | Disattiva l'IME quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**\_FORCENONE FMI**</dt> </dl>                         | Disabilita la gestione IME.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**\_FORCEREMEMBER FMI**</dt> </dl>             | Ripristina lo stato dell'IME precedente quando il controllo riceve lo stato attivo per l'input.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**\_MULTIPLEEDIT FMI**</dt> </dl>                | Specifica che la stringa di composizione non verrà annullata o determinata dalla modifica dello stato attivo. Questo consente a un'applicazione di avere stringhe di composizione separate in ogni controllo Rich Edit.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**FMI \_ verticale**</dt> </dl>                            | Nota utilizzata in Rich Edit 2,0 e versioni successive. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETIMEOPTIONS em**](em-getimeoptions.md)
</dt> </dl>

 

 





