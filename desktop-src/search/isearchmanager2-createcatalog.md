---
description: Crea un nuovo catalogo personalizzato nell'indicizzatore di ricerca di Windows e ne restituisce un riferimento.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'Metodo ISearchManager2:: CreateCatalog'
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
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225944"
---
# <a name="isearchmanager2createcatalog-method"></a>Metodo ISearchManager2:: CreateCatalog

Crea un nuovo catalogo personalizzato nell'indicizzatore di ricerca di Windows e ne restituisce un riferimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszCatalog* \[ in\]
</dt> <dd>

Tipo: **[ **LPCWSTR**](../winprog/windows-data-types.md)**

Nome del catalogo da creare. Può essere qualsiasi nome selezionato dal chiamante, deve contenere solo caratteri alfanumerici standard e carattere di sottolineatura.

</dd> <dt>

*ppCatalogManager* \[ out\]
</dt> <dd>

Tipo: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

In seguito all'esito positivo, un riferimento al catalogo creato viene restituito come puntatore di interfaccia [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . Il rilascio () deve essere chiamato su questa interfaccia dopo che l'applicazione chiamante ha terminato di utilizzarla.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

HRESULT che indica lo stato dell'operazione:



| Codice restituito                                                                             | Descrizione                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Il catalogo non esisteva in precedenza ed è stato creato. Riferimento al catalogo restituito.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Catalogo in precedenza esistente. riferimento al catalogo restituito.<br/>                       |



 

HRESULT non riuscito: errore durante la creazione del catalogo o degli argomenti non validi.

## <a name="remarks"></a>Commenti

Chiamato per creare un nuovo catalogo nell'indicizzatore di ricerca di Windows. Dopo la creazione, è possibile usare i metodi del gestore [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) restituito per aggiungere percorsi da indicizzare, monitorare il processo di indicizzazione e creare query da inviare all'indicizzatore e ottenere risultati. Per ulteriori informazioni, vedere la documentazione relativa alla gestione dell'indice: https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
