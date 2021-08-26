---
title: Metodo ISearchDesktop ExecuteSQLQuery
description: Accetta un puntatore a una stringa che contiene una query Structured Query Language (SQL) e i relativi attributi e restituisce un puntatore al set restituito.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Metodo ExecuteSQLQuery Funzionalità dell'Windows legacy
- Metodo ExecuteSQLQuery Legacy Windows Environment Features , interfaccia ISearchDesktop
- Interfaccia ISearchDesktop Legacy Windows Environment Features , metodo ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec436a427958988e7605673b12b3fd8dc6fd3e1a54ab61cc5f542f0494c34923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014291"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>Metodo ISearchDesktop::ExecuteSQLQuery

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Accetta un puntatore a una stringa che contiene una query Structured Query Language (SQL) e i relativi attributi e restituisce un puntatore al set restituito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwAttributes* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR \***

Stringa che contiene gli altri attributi per la query.

</dd> <dt>

*pwszURL* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Stringa che contiene la SQL query.

</dd> <dt>

*ppidUrl* \[ Cambio\]
</dt> <dd>

Tipo: **ppidUrl \***

Quando questo metodo viene restituito correttamente, contiene un puntatore al recordset restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

 

 




