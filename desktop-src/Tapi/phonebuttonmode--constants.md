---
description: Le \_ costanti del flag di bit PHONEBUTTONMODE descrivono le classi di pulsanti.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: Costanti PHONEBUTTONMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4ee5e9835b7df06773bc1429641c91597c15e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333956"
---
# <a name="phonebuttonmode_-constants"></a>\_Costanti PHONEBUTTONMODE

Le costanti del flag di bit **PHONEBUTTONMODE \_** descrivono le classi di pulsanti.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**\_chiamata PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Il pulsante viene assegnato a un aspetto della chiamata.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**\_visualizzazione PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Il pulsante è un pulsante "soft" associato alla visualizzazione del telefono. Un set di telefono può contenere zero o più pulsanti di visualizzazione.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**\_manichino PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Questo valore viene usato per descrivere la posizione di un pulsante o di una lampada senza pulsante corrispondente ma con solo una lampada.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**\_funzionalità PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Il pulsante viene assegnato alle funzionalità richieste dal commutatore, ad esempio attesa, conferenza e trasferimento.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**\_tastiera PHONEBUTTONMODE**
</dt> <dd> <dl> <dt>



Il pulsante è uno dei dodici pulsanti del tastierino, compreso tra 0 e 9,' \* ' è \# '.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ locale**
</dt> <dd> <dl> <dt>



Il pulsante è un pulsante della funzione locale, ad esempio mute o controllo volume.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Questo tipo di enumerazione viene utilizzato nella struttura dei dati [**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) per descrivere il significato associato ai pulsanti del telefono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




