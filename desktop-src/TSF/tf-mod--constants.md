---
title: Costanti TF_MOD_ (msctf. h)
description: Le \_ costanti TF mod \_ \ specificano i modificatori di chiave nella \_ struttura TF PRESERVEDKEY.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048325"
---
# <a name="tf_mod_-constants"></a>\_Costanti TF mod \_ \*

Le \_ costanti TF mod \_ \* specificano i modificatori di chiave nella struttura [tf \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .



| Costante/valore                                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <dt>**Tf \_ MOD \_ ALT**</dt> <dt>0x0001</dt> </dl>                                                   | Viene premuto uno dei tasti ALT<br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <dt>**Tf \_ \_Controllo mod**</dt> <dt>0x0002</dt> </dl>                                       | Viene premuto uno dei tasti CTRL<br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <dt>**Tf \_ MOD \_ Shift**</dt> <dt>0x0004</dt> </dl>                                             | Viene premuto uno dei tasti MAIUSC<br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <dt>**Tf \_ MOD \_ Ralt**</dt> <dt>0x0008</dt> </dl>                                                | Viene premuto il tasto ALT destro<br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <dt>**Tf \_ MOD \_ RCONTROL**</dt> <dt>0x0010</dt> </dl>                                    | Viene premuto il tasto CTRL destro<br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <dt>**Tf \_ MOD \_ RSHIFT**</dt> <dt>0x0020</dt> </dl>                                          | Viene premuto il tasto MAIUSC destro<br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <dt>**Tf \_ MOD \_ LALT**</dt> <dt>0x0040</dt> </dl>                                                | Viene premuto il tasto ALT sinistro<br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <dt>**Tf \_ MOD \_ LCONTROL**</dt> <dt>0x0080</dt> </dl>                                    | Viene premuto il tasto CTRL sinistro<br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <dt>**Tf \_ MOD \_ LSHIFT**</dt> <dt>0x0100</dt> </dl>                                          | Viene premuto il tasto MAIUSC sinistro<br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <dt>**Tf \_ MOD \_ su \_ KEYUP**</dt> <dt>0x0200</dt> </dl>                                   | L'evento verrà generato quando la chiave viene rilasciata. Senza questo flag, l'evento viene generato quando viene premuto il tasto.<br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <dt>**Tf \_ MOD \_ Ignora \_ tutti i \_ modificatori**</dt> <dt>0x0400</dt> </dl> | Lo stato dei tasti ALT, CTRL e MAIUSC viene ignorato. Ciò significa che l'evento verrà generato quando viene premuto il tasto virtuale, indipendentemente dai tasti di modifica.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_PRESERVEDKEY TF](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





