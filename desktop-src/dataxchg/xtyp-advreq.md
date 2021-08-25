---
title: XTYP_ADVREQ transazione (Ddeml.h)
description: La transazione XTYP ADVREQ informa il server che una transazione di consulenza è in sospeso nella coppia nome argomento e nome elemento specificata e che i dati corrispondenti alla coppia nome argomento e nome elemento \_ sono stati modificati.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ dati della transazione Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e751f17fb8634b0a105a36af5036f07d0212532349c267e5526d5d41f09367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544886"
---
# <a name="xtyp_advreq-transaction"></a>Transazione \_ ADVREQ XTYP

La **transazione XTYP \_ ADVREQ** informa il server che una transazione di consulenza è in sospeso nella coppia nome argomento e nome elemento specificata e che i dati corrispondenti alla coppia nome argomento e nome elemento sono stati modificati. Il sistema invia questa transazione alla funzione di callback Dynamic Data Exchange [*(DDE), DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), dopo che il server ha chiamato la funzione [**DdePostAdvise.**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Formato in cui i dati devono essere inviati al client.

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

Handle per il nome dell'elemento modificato.

</dd> <dt>

*hdata* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData1* 
</dt> <dd>

Conteggio, nella parola di ordine basso, delle transazioni **\_ XTYP ADVREQ** che rimangono da elaborare nello stesso argomento, elemento e nome di formato impostati nel contesto della chiamata corrente alla funzione [**DdePostAdvise.**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) Il conteggio è zero se la transazione **\_ XTYP ADVREQ** corrente è l'ultima. Un server può usare questo conteggio per determinare se creare un handle di dati **HDATA \_ APPOWNED** per i dati di consulenza.

La parola di ordine basso è impostata su **CADV \_ LATEACK** se il DDEML ha emesso la transazione **\_ XTYP ADVREQ** a causa di un messaggio DDE ACK in arrivo in ritardo da un client in uscita dal \_ server.

La parola di ordine alto non viene usata.

</dd> <dt>

*dwData2* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il server deve prima chiamare la [**funzione DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) per creare un handle di dati che identifica i dati modificati e quindi restituire l'handle. Il server deve restituire **NULL** se non è in grado di completare la transazione.

## <a name="remarks"></a>Commenti

Un server non può bloccare questo tipo di transazione. Il **codice restituito CBR \_ BLOCK** viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Ddeml.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

