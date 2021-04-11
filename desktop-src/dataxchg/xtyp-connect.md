---
title: Transazione XTYP_CONNECT (DDEML. h)
description: Un client usa la \_ transazione di connessione XTYP per stabilire una conversazione.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- Scambio di dati delle transazioni XTYP_CONNECT
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120035"
---
# <a name="xtyp_connect-transaction"></a>\_Transazione di connessione XTYP

Un client usa la transazione di **\_ connessione XTYP** per stabilire una conversazione. Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica un nome di servizio supportato dal server (e un nome di argomento non **null**) in una chiamata alla funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uType* 
</dt> <dd>

Tipo di transazione.

</dd> <dt>

*uFmt* 
</dt> <dd>

Non usato.

</dd> <dt>

*hconv* 
</dt> <dd>

Non usato.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle per il nome dell'argomento.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome del servizio.

</dd> <dt>

*hdata* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData1* 
</dt> <dd>

Puntatore a una struttura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) che contiene informazioni di contesto per la conversazione. Se il client non è un'applicazione DDEML, questo parametro è 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Specifica se il client è la stessa istanza dell'applicazione del server. Se il parametro è 1, il client è la stessa istanza. Se il parametro è 0, il client è un'istanza diversa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una funzione di callback del server deve restituire **true** per consentire al client di stabilire una conversazione con il nome del servizio e la coppia di nomi di argomento specificati oppure la funzione deve restituire **false** per negare la conversazione. Se la funzione di callback restituisce **true** e una conversazione viene stabilita correttamente, il sistema passa l'handle di conversazione al server eseguendo una [**XTYP \_ Connect \_ Confirm**](xtyp-connect-confirm.md) Transaction per la funzione di callback del server, a meno che il server non abbia specificato il flag **CBF \_ Skip \_ Connect \_ confirms** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ Connections** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un server non è in grado di bloccare questo tipo di transazione. il codice restituito del **\_ blocco CBR** viene ignorato.

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

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

