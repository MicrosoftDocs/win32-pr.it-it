---
title: Metodo ISearchDesktop ExecuteSQLQuery
description: Accetta un puntatore a una stringa che contiene una query Structured Query Language (SQL) e i relativi attributi e restituisce un puntatore al set restituito.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Funzionalità dell'ambiente Windows legacy del metodo ExecuteSQLQuery
- Funzionalità dell'ambiente Windows legacy del metodo ExecuteSQLQuery, interfaccia ISearchDesktop
- Funzionalità dell'ambiente Windows legacy dell'interfaccia ISearchDesktop, metodo ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724012"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>Metodo ISearchDesktop:: ExecuteSQLQuery

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Accetta un puntatore a una stringa che contiene una query Structured Query Language (SQL) e i relativi attributi e restituisce un puntatore al set restituito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwAttributes* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR \***

Stringa contenente gli altri attributi per la query.

</dd> <dt>

*pwszURL* \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Stringa che contiene la query SQL.

</dd> <dt>

*ppidUrl* \[ out\]
</dt> <dd>

Tipo: **ppidUrl \***

Quando questo metodo viene restituito correttamente, contiene un puntatore al recordset restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

 

 




