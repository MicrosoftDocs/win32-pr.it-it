---
title: Transazione XTYP_ADVSTART (DDEML. h)
description: Un client utilizza la \_ transazione XTYP ADVSTART per stabilire un ciclo di notifica con un server.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- Scambio di dati delle transazioni XTYP_ADVSTART
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741858"
---
# <a name="xtyp_advstart-transaction"></a>\_Transazione ADVSTART XTYP

Un client utilizza la transazione **XTYP \_ ADVSTART** per stabilire un ciclo di notifica con un server. Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica **XTYP \_ ADVSTART** come parametro *wType* della funzione [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Formato dati richiesto dal client.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle per la conversazione.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle per il nome dell'argomento.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome dell'elemento.

</dd> <dt>

*hdata* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData2* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una funzione di callback del server deve restituire **true** per consentire un ciclo di notifica sul nome dell'argomento e sulla coppia di nomi di elemento specificati oppure su **false** per negare il ciclo di notifica. Se la funzione di callback restituisce **true**, tutte le chiamate successive alla funzione [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) da parte del server nella stessa coppia nome argomento e nome elemento fanno sì che il sistema invii le transazioni [**\_ ADVREQ XTYP**](xtyp-advreq.md) al server.

## <a name="remarks"></a>Commenti

Se un client richiede un ciclo di notifica per un nome di argomento, un nome di elemento e un formato dati per un ciclo di notifica già stabilito, la libreria di gestione Dynamic Data Exchange (DDEML) non crea un ciclo di notifica duplicato, ma modifica i flag del ciclo di notifica (**XTYPF \_ ACKREQ** e **XTYPF \_ NoData**) in modo che corrispondano alla richiesta più recente.

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ advises** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>DDEML. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

