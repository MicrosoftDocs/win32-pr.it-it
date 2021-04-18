---
title: Struttura WMDMMetadataView
description: La struttura WMDMMetadataView definisce la visualizzazione dei metadati. Il contenuto è organizzato in base a questa definizione.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- Struttura WMDMMetadataView Windows Media Gestione dispositivi
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
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324402"
---
# <a name="wmdmmetadataview-structure"></a>Struttura WMDMMetadataView

La struttura **WMDMMetadataView** definisce la visualizzazione dei metadati. Il contenuto è organizzato in base a questa definizione.

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

Puntatore a una stringa a caratteri wide con terminazione null che contiene il nome della visualizzazione. Viene utilizzato come nome del nodo radice in cui viene presentata la visualizzazione.

</dd> <dt>

**nDepth**
</dt> <dd>

Integer contenente la profondità della visualizzazione, che indica il numero di tag di metadati annidati utilizzati per la visualizzazione.

</dd> <dt>

**ppwszTags**
</dt> <dd>

Matrice di stringhe di tag dei metadati per i tag annidati.

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



Il codice precedente organizza il contenuto come segue:

<dl> Visualizzazione personale<dl> Genre1<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture**](structures.md)
</dt> </dl>

 

 





