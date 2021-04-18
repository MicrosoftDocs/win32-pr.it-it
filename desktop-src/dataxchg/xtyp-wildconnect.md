---
title: Transazione XTYP_WILDCONNECT (DDEML. h)
description: Consente a un client di stabilire una conversazione su ognuna delle coppie nome servizio e nome argomento del server che corrispondono al nome del servizio e al nome dell'argomento specificati.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- Scambio di dati delle transazioni XTYP_WILDCONNECT
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301595"
---
# <a name="xtyp_wildconnect-transaction"></a>\_Transazione WILDCONNECT XTYP

Consente a un client di stabilire una conversazione su ognuna delle coppie nome servizio e nome argomento del server che corrispondono al nome del servizio e al nome dell'argomento specificati. Una funzione di callback del server Dynamic Data Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), riceve questa transazione quando un client specifica un nome di servizio **null** , un nome di argomento **null** o entrambi in una chiamata alla funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) o [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
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

Handle per il nome dell'argomento. Se questo parametro è **null**, il client richiede una conversazione su tutti i nomi di argomento supportati dal server.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle per il nome del servizio. Se questo parametro è **null**, il client richiede una conversazione su tutti i nomi di servizio supportati dal server.

</dd> <dt>

*hdata* 
</dt> <dd>

Non usato.

</dd> <dt>

*dwData1* 
</dt> <dd>

Puntatore a una struttura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) che contiene informazioni di contesto per la conversazione. Se il client non è un'applicazione DDEML, questo parametro è impostato su 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Specifica se il client è la stessa istanza dell'applicazione del server. Se il parametro è 1, il client è la stessa istanza. Se il parametro è 0, il client è un'istanza diversa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il server deve restituire un handle di dati che identifichi una matrice di strutture [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) . La matrice deve contenere una struttura per ogni coppia nome-servizio e nome-argomento che corrisponde alla coppia nome-servizio e nome-argomento richiesta dal client. La matrice deve terminare con un handle di stringa **null** . Il sistema invia la transazione di [**\_ \_ conferma XTYP Connect**](xtyp-connect-confirm.md) al server per confermare ogni conversazione e passare gli handle di conversazione al server. Il server non riceverà queste conferme se ha specificato il flag **CBF \_ Skip \_ Connect \_ confirms** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Il server deve restituire **null** per rifiutare la **transazione \_ WILDCONNECT XTYP** .

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ Fail \_ Connections** nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un server non è in grado di bloccare questo tipo di transazione. il \_ codice restituito del blocco CBR viene ignorato.

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

[**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di gestione Dynamic Data Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

