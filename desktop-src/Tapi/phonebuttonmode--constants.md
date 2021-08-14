---
description: Le costanti del flag di bit PHONEBUTTONMODE \_ descrivono le classi di pulsanti.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: PHONEBUTTONMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9424c23a9fe6497c657081dd9e197526dc5eb897ad773b1e03fb33c9f08113df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761303"
---
# <a name="phonebuttonmode_-constants"></a>Costanti \_ PHONEBUTTONMODE

Le costanti del flag di bit **PHONEBUTTONMODE \_** descrivono le classi di pulsanti.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**CHIAMATA \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Il pulsante viene assegnato all'aspetto di una chiamata.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**VISUALIZZAZIONE \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Il pulsante è un pulsante "soft" associato allo schermo del telefono. Un set di telefoni può avere zero o più pulsanti di visualizzazione.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE \_ FITTIZIO**
</dt> <dd> <dl> <dt>



Questo valore viene usato per descrivere la posizione di un pulsante/lampione che non ha un pulsante corrispondente ma ha solo una lampione.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**FUNZIONALITÀ \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Il pulsante viene assegnato alla richiesta di funzionalità dal commutatore, ad esempio attesa, conferenza e trasferimento.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**TASTIERA \_ PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Il pulsante è uno dei dodici pulsanti del tastierino, da 0 a 9, ' \* ' e ' \# '.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ LOCAL**
</dt> <dd> <dl> <dt>



Il pulsante è un pulsante di funzione locale, ad esempio l'audio o il controllo del volume.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Questo tipo di enumerazione viene usato nella struttura dei dati [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) per descrivere il significato associato ai pulsanti del telefono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




