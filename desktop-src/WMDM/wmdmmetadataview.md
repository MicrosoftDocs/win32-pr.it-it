---
title: Struttura WMDMMetadataView
description: La struttura WMDMMetadataView definisce la visualizzazione dei metadati. Il contenuto è organizzato in base a questa definizione.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Struttura WMDMMetadataView windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e442ed3058f1982ac7607c6b8a29e5df321d69776695821b278049e27cd7589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862591"
---
# <a name="wmdmmetadataview-structure"></a>Struttura WMDMMetadataView

La **struttura WMDMMetadataView** definisce la visualizzazione dei metadati. Il contenuto è organizzato in base a questa definizione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a>Members

<dl> <dt>

**pwszViewName**
</dt> <dd>

Puntatore a una stringa con terminazione Null a caratteri wide contenente il nome della vista. Viene usato come nome del nodo radice in cui viene presentata la vista.

</dd> <dt>

**Ndepth**
</dt> <dd>

Intero contenente la profondità della vista, che indica il numero di tag di metadati annidati usati per la vista.

</dd> <dt>

**ppwszTags**
</dt> <dd>

Matrice di stringhe di tag di metadati per i tag annidati.

</dd> </dl>

## <a name="examples"></a>Esempio

Il codice seguente crea una visualizzazione dei metadati:


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



Il codice precedente organizza il contenuto nel modo seguente:

<dl> Visualizzazione personalizzata<dl> Genre1<dl> Artista1<dl> Album1<dl> Brano 1  
Brano2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Brano 1  
Brano2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artista1<dl> Album1<dl> Brano 1  
Brano2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Brano 1  
Brano2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





