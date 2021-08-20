---
title: PSM_GETRESULT messaggio (Prsht.h)
description: Utilizzato dalle finestre delle proprietà non modali per recuperare le informazioni restituite alle finestre delle proprietà modali da PropertySheet. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro PropSheet GetResult.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- PSM_GETRESULT controlli Windows messaggio
topic_type:
- apiref
api_name:
- PSM_GETRESULT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acc8fed8cdaa1f4282c3ed066ad44f68221330fa9e79b0719db8bba1bca37f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169807"
---
# <a name="psm_getresult-message"></a>Messaggio \_ GETRESULT PSM

Utilizzato dalle finestre delle proprietà non modali per recuperare le informazioni restituite alle finestre delle proprietà modali [**da PropertySheet.**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet GetResult.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore positivo in caso di esito positivo oppure -1 in caso contrario. I valori restituiti seguenti hanno un significato speciale.



| Codice restituito                                                                                         | Descrizione                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Una pagina ha inviato un [**messaggio \_ REBOOTSYSTEM PSM**](psm-rebootsystem.md) alla finestra delle proprietà. Per l'applicazione delle modifiche dell'utente, è necessario riavviare il computer.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Una pagina ha inviato un [**messaggio \_ RESTARTWINDOWS PSM**](psm-restartwindows.md) alla finestra delle proprietà. Windows necessario riavviare per l'applicazione delle modifiche dell'utente.<br/>  |



 

## <a name="remarks"></a>Commenti

Per recuperare informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Il valore restituito per questo messaggio è identico a quello restituito da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) per una finestra delle proprietà modale.

[Versione 5.80.](common-control-versions.md) Il [**valore restituito PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) contiene informazioni diverse per le finestre delle proprietà modali e non modali. In alcuni casi, le finestre delle proprietà non modali potrebbero richiedere le informazioni che avrebbero ricevuto da **PropertySheet** se fossero state modali. In particolare, potrebbe essere necessario sapere se sarebbe stato restituito \_ l'ID PSREBOOTSYSTEM o \_ l'ID PSRESTARTWINDOWS.

Per una finestra delle proprietà non modali, il ciclo di messaggi deve usare [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) per passare i messaggi alla finestra delle proprietà e [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) per determinare quando eliminare la finestra di dialogo. Quando l'utente fa clic sul **pulsante OK** o **Annulla,** **PSM \_ GETCURRENTPAGEHWND** restituisce **NULL.** È quindi possibile recuperare il valore ricevuto da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) da una finestra delle proprietà modale inviando un **messaggio \_ GETRESULT PSM.**

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ ACROBATWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

