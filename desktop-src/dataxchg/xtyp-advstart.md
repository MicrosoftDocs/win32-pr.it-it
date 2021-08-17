---
title: XTYP_ADVSTART transazione (Ddeml.h)
description: Un client usa la transazione ADVSTART XTYP \_ per stabilire un ciclo di consulenza con un server.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART di dati della Exchange
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
ms.openlocfilehash: fb18bda3dce4db465045991e26cdc2d97ddd87ddc69c494ffaf103c566955da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544760"
---
# <a name="xtyp_advstart-transaction"></a>Transazione \_ ADVSTART XTYP

Un client usa la **transazione \_ ADVSTART XTYP** per stabilire un ciclo di consulenza con un server. Una funzione di callback del server Dynamic Data Exchange [*(DDE), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)riceve questa transazione quando un client specifica **XTYP \_ ADVSTART** come parametro *wType* della [**funzione DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


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

Formato dei dati richiesto dal client.

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

Una funzione di callback del server deve restituire **TRUE** per consentire un ciclo di consulenza sulla coppia nome argomento e nome elemento specificata oppure **FALSE** per negare il ciclo di consulenza. Se la funzione di callback restituisce **TRUE,** qualsiasi chiamata successiva alla funzione [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) da parte del server nella stessa coppia nome argomento e nome elemento fa sì che il sistema invii le transazioni [**\_ ADVREQ XTYP**](xtyp-advreq.md) al server.

## <a name="remarks"></a>Commenti

Se un client richiede un ciclo di consulenza per un nome di argomento, un nome di elemento e un formato di dati per un ciclo di consulenza già stabilito, la libreria di gestione di Dynamic Data Exchange (DDEML) non crea un ciclo di consulenza duplicato, ma modifica i flag di ciclo di consulenza (**XTYPF \_ ACKREQ** e **XTYPF \_ NODATA)** in modo che corrispondano alla richiesta più recente.

Questa transazione viene filtrata se l'applicazione server ha specificato il flag **CBF \_ FAIL \_ ADVISES** nella [**funzione DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

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

[**Ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Dynamic Data Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

