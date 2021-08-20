---
title: Recupero dell'attributo objectClass
description: L'attributo objectClass contiene la classe di cui l'oggetto è un'istanza, nonché tutte le classi da cui tale classe è derivata.
ms.assetid: 6066d9c3-f97b-482a-88c7-0fde1dc2f4c4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c4ae206298937839a965eca787b0d56b0021cff32c7d89b06865bb27855a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184142"
---
# <a name="retrieving-the-objectclass-attribute"></a>Recupero dell'attributo objectClass

**L'attributo objectClass** contiene la classe di cui l'oggetto è un'istanza, nonché tutte le classi da cui tale classe è derivata. Ad esempio, la **classe utente** eredita da **top**, **person** e **organizationalPerson**; Pertanto, **l'attributo objectClass** contiene i nomi di tali classi, nonché l'utente. Quindi, come è possibile individuare la classe di cui l'oggetto è un'istanza? **L'attributo objectClass** è l'unico attributo con più valori con valori ordinati. Il primo valore è la parte superiore della gerarchia di classi, ovvero la classe principale, e l'ultimo valore è la classe più derivata, ovvero la classe di cui l'oggetto è un'istanza.

La funzione seguente accetta un puntatore a una colonna contenente un **attributo objectClass** e restituisce l'oggetto **objectClass di** cui è stata creata un'istanza dell'oggetto.


```C++
HRESULT GetClass(ADS_SEARCH_COLUMN *pcol, LPOLESTR *ppClass)
{
  if (!pcol)
    return E_POINTER;
 
  HRESULT hr = E_FAIL;
  if (ppClass)
  {
    LPOLESTR szClass = new OLECHAR[MAX_PATH];
    wcscpy_s(szClass, L"");
    if ( _wcsicmp(pcol->pszAttrName,L"objectClass") == 0 )
    {
      for (DWORD x = 0; x< pcol->dwNumValues; x++)
      {
        wcscpy_s(szClass, pcol->pADsValues[x].CaseIgnoreString);
      }
    }
    if (0==wcscmp(L"", szClass))
    {
      hr = E_FAIL;
    }
    else
    {
      //Allocate memory for string.
      //Caller must free using CoTaskMemFree.
      *ppClass = (OLECHAR *)CoTaskMemAlloc (
                             sizeof(OLECHAR)*(wcslen(szClass)+1));
      if (*ppClass)
      {
        wcscpy_s(*ppClass, szClass);
        hr = S_OK;
      }
      else
      hr=E_FAIL;
    }
  }
  return hr;
}
```



 

 




