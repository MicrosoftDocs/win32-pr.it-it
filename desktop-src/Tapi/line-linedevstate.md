---
description: Il messaggio della linea TAPI \_ LINEDEVSTATE viene inviato quando lo stato di un dispositivo a linee è cambiato. L'applicazione può richiamare lineGetLineDevStatus per determinare il nuovo stato della riga.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: Messaggio di LINE_LINEDEVSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327404"
---
# <a name="line_linedevstate-message"></a>\_Messaggio linea LINEDEVSTATE

Il messaggio della **linea TAPI \_ LINEDEVSTATE** viene inviato quando lo stato di un dispositivo a linee è cambiato. L'applicazione può richiamare [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) per determinare il nuovo stato della riga.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per il dispositivo della linea. Questo parametro è **null** se *dwParam1* è LINEDEVSTATE \_ reinit.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga. Se il parametro *dwParam1* è LINEDEVSTATE \_ reinit, il parametro *dwCallbackInstance* non è valido e è impostato su zero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Elemento di stato del dispositivo di linea modificato. Il parametro può essere costituito da una o [**più \_ costanti LINEDEVSTATE**](linedevstate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

L'interpretazione di questo parametro dipende dal valore di *dwParam1*. Se *dwParam1* è LINEDEVSTATE \_ Ringing, *dwParam2* contiene la modalità ring con cui l'opzione indica alla riga di squillare. Le modalità anello valide sono numeri nell'intervallo da uno a **dwNumRingModes**, dove **dwNumRingModes** è una funzionalità di dispositivo linea.

Se *dwParam1* è LINEDEVSTATE \_ reinit e il messaggio è stato emesso da TAPI come risultato della conversione di un nuovo messaggio API in un messaggio reinit, *DwParam2* contiene il parametro *dwMsg* del messaggio originale (ad esempio, [**riga \_ creazione**](line-create.md) o riga \_ LINEDEVSTATE). Se *dwParam2* è zero, questo indica che il messaggio reinit è un messaggio "Real" reinit che richiede che l'applicazione chiami [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) alla prima convenienza.

</dd> <dt>

*dwParam3* 
</dt> <dd>

L'interpretazione di questo parametro dipende dal valore di *dwParam1*. Se *dwParam1* è LINEDEVSTATE \_ Ringing, *dwParam3* contiene il numero di squilli per questo evento ring. Il numero di squilli inizia da zero.

Se *dwParam1* è LINEDEVSTATE \_ reinit e il messaggio è stato emesso da TAPI come risultato della conversione di un nuovo messaggio API in un messaggio reinit, *DwParam3* contiene il parametro *dwParam1* del messaggio originale (ad esempio, LINEDEVSTATE \_ TRANSLATECHANGE o un altro \_ valore LINEDEVSTATE, se *dwParam2* è la riga LINEDEVSTATE o \_ il nuovo identificatore di dispositivo, se *dwParam2* è [**line \_ create**](line-create.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'invio del messaggio di **riga \_ LINEDEVSTATE** può essere controllato con [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages). Un'applicazione può indicare le modifiche degli elementi di stato per le quali si desidera ricevere una notifica. Per impostazione predefinita, tutti i rapporti di stato sono disabilitati, ad eccezione di LINEDEVSTATE \_ reinit, che non può essere disabilitato. Questo messaggio viene inviato a tutte le applicazioni che dispongono di un handle per la riga, inclusi quelli che hanno chiamato [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) con il parametro *DWPRIVILEGES* impostato su LINECALLPRIVILEGE \_ None, LINECALLPRIVILEGE \_ Owner, LINECALLPRIVILEGE \_ monitor o combinazioni consentite di questi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_chiusura riga**](line-close.md)
</dt> <dt>

[**\_creazione linea**](line-create.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




