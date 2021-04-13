---
title: Messaggio PSM_GETRESULT (Prsht. h)
description: Utilizzato dalle finestre delle proprietà non modali per recuperare le informazioni restituite alle finestre delle proprietà modali da PropertySheet. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetResult PropSheet.
ms.assetid: e0f609ea-5d7e-4c17-ade1-3c1051c5a5bf
keywords:
- Controlli di Windows Message PSM_GETRESULT
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
ms.openlocfilehash: d41609f625cbd3938fa78e9a2f91ab70168ecc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518531"
---
# <a name="psm_getresult-message"></a>\_Messaggio PSM GETresult

Utilizzato dalle finestre delle proprietà non modali per recuperare le informazioni restituite alle finestre delle proprietà modali da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetResult PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getresult) .

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

Restituisce un valore positivo se ha esito positivo oppure-1 in caso contrario. I valori restituiti riportati di seguito hanno un significato speciale.



| Codice restituito                                                                                         | Descrizione                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ID \_ PSREBOOTSYSTEM**</dt> </dl>   | Una pagina ha inviato un messaggio [**PSM \_ REBOOTSYSTEM**](psm-rebootsystem.md) alla finestra delle proprietà. Per rendere effettive le modifiche dell'utente, è necessario riavviare il computer.<br/> |
| <dl> <dt>**ID \_ PSRESTARTWINDOWS**</dt> </dl> | Una pagina ha inviato un messaggio [**PSM \_ RESTARTWINDOWS**](psm-restartwindows.md) alla finestra delle proprietà. È necessario riavviare Windows per rendere effettive le modifiche dell'utente.<br/>  |



 

## <a name="remarks"></a>Commenti

Per recuperare informazioni estese sugli errori, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Il valore restituito per questo messaggio è identico a quello restituito da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) per una finestra delle proprietà modale.

[Versione 5,80.](common-control-versions.md) Il valore restituito [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) contiene informazioni diverse per le finestre delle proprietà modali e non modali. In alcuni casi, le finestre delle proprietà non modali possono richiedere le informazioni ricevute da **PropertySheet** se fossero modali. In particolare, potrebbe essere necessario sapere se \_ è stato restituito ID PSREBOOTSYSTEM o ID \_ PSRESTARTWINDOWS.

Per una finestra delle proprietà non modale, il ciclo di messaggi deve usare [**PSM \_ ISDIALOGMESSAGE**](psm-isdialogmessage.md) per passare i messaggi alla finestra di dialogo della finestra delle proprietà e [**PSM \_ GETCURRENTPAGEHWND**](psm-getcurrentpagehwnd.md) per determinare quando eliminare la finestra di dialogo. Quando l'utente fa clic sul pulsante **OK** o **Annulla** , **PSM \_ GETCURRENTPAGEHWND** restituisce **null**. È quindi possibile recuperare il valore ricevuto da una finestra delle proprietà modale da [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) inviando un messaggio **PSM \_ GetResult** .

> [!Note]  
> Questo messaggio non è supportato quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

