---
title: XTYP_CONNECT transazione (Ddeml.h)
description: Un client usa la transazione XTYP \_ CONNECT per stabilire una conversazione.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT dati della transazione Exchange
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
ms.openlocfilehash: c1ff7a7a79d8b61deef6b5f19b829e5c8dd8f4603c5f60c3b47d0a84b0603736
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793421"
---
# <a name="xtyp_connect-transaction"></a>Transazione XTYP \_ CONNECT

Un client usa la **transazione XTYP \_ CONNECT** per stabilire una conversazione. Una funzione di callback del server Dynamic Data Exchange [*(DDE), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)riceve questa transazione quando un client specifica un nome di servizio che il server supporta (e un nome di argomento diverso da **NULL)** in una chiamata alla [**funzione DdeConnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)


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

Puntatore a una [**struttura CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) che contiene informazioni di contesto per la conversazione. Se il client non è un'applicazione DDEML, questo parametro è 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Specifica se il client è la stessa istanza dell'applicazione del server. Se il parametro è 1, il client è la stessa istanza. Se il parametro è 0, il client è un'istanza diversa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Una funzione di callback del server deve restituire **TRUE** per consentire al client di stabilire una conversazione sulla coppia nome servizio e nome argomento specificata oppure la funzione deve restituire **FALSE** per negare la conversazione. Se la funzione di callback restituisce **TRUE** e una conversazione viene stabilita correttamente, il sistema passa l'handle di conversazione al server emettendo una transazione [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) alla funzione di callback del server (a meno che il server non specificasse il flag **CBF \_ SKIP CONNECT \_ \_ CONFIRMS** nella [**funzione DdeInitialize).**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

## <a name="remarks"></a>Commenti

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ FAIL \_ CONNECTIONS** nella [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Un server non può bloccare questo tipo di transazione. Il **codice restituito da CBR \_ BLOCK** viene ignorato.

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

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

