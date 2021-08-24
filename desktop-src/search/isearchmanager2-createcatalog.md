---
description: Crea un nuovo catalogo personalizzato nell'Windows indicizzatore di ricerca e restituisce un riferimento a esso.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: Metodo ISearchManager2::CreateCatalog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 34a4ceb37045ebbae62e04da0b5395673ed498c56189a26f2abaa376c960c511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597751"
---
# <a name="isearchmanager2createcatalog-method"></a>Metodo ISearchManager2::CreateCatalog

Crea un nuovo catalogo personalizzato nell'Windows indicizzatore di ricerca e restituisce un riferimento a esso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszCatalog* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCWSTR**](../winprog/windows-data-types.md)**

Nome del catalogo da creare. Può essere qualsiasi nome selezionato dal chiamante e deve contenere solo caratteri alfanumerici e caratteri di sottolineatura standard.

</dd> <dt>

*ppCatalogManager* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

Se l'operazione ha esito positivo, viene restituito un riferimento al catalogo creato come [**puntatore a interfaccia ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) Release() deve essere chiamato su questa interfaccia dopo che l'applicazione chiamante ha terminato di usarla.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

HRESULT che indica lo stato dell'operazione:



| Codice restituito                                                                             | Descrizione                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Il catalogo non esisteva in precedenza ed è stato creato. Riferimento al catalogo restituito.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Catalog esisteva in precedenza, riferimento al catalogo restituito.<br/>                       |



 

FAILED HRESULT: errore durante la creazione del catalogo o argomenti non validi passati.

## <a name="remarks"></a>Commenti

Chiamato per creare un nuovo catalogo nell'indicizzatore Windows ricerca. Dopo la creazione, i metodi nella gestione [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) restituita possono essere usati per aggiungere percorsi da indicizzare, monitorare il processo di indicizzazione e costruire query da inviare all'indicizzatore e ottenere risultati. Per altre informazioni, vedere la documentazione "Gestione dell'indice": https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>           |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
