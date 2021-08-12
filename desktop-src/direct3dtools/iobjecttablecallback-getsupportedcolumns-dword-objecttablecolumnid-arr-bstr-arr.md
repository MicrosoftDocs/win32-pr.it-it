---
description: Ottiene informazioni sulle colonne (tipi di dati oggetto) supportate dalla tabella oggetti.
MS-HAID: vspixengine.IObjectTableCallback\_GetSupportedColumns\_DWORD\_ObjectTableColumnID\_arr\_BSTR\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IObjectTableCallback::GetSupportedColumns
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 148AB80D-9833-4B57-9F34-CEDFFF8E905A
api_name:
- IObjectTableCallback.GetSupportedColumns
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6f785c8fafadf62a874d6be1d4c3ab2092f9cdaf8b49cc40f826b42fb69ce3b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283236"
---
# <a name="span-idvspixengineiobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arrspaniobjecttablecallbackgetsupportedcolumns-method"></a><span id="vspixengine.iobjecttablecallback_getsupportedcolumns_dword_objecttablecolumnid_arr_bstr_arr"></span>Metodo IObjectTableCallback::GetSupportedColumns

Ottiene informazioni sulle colonne (tipi di dati oggetto) supportate dalla tabella oggetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSupportedColumns(
   DWORD                  numColumns,
   ObjectTableColumnID [] count0_pIDs,
   BSTR []                count0_pBstrNames
);
```

## <a name="parameters"></a>Parametri

*Numcolumns*   
Numero di colonne supportate dalla tabella oggetto.

*count0_pIDs*   
ID di ogni colonna supportata dalla tabella dell'oggetto.

*count0_pBstrNames*   
Nomi di ogni colonna, come stringa COM, supportati dalla tabella di oggetti.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, **restituisce** S_OK . In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IObjectTableCallback**](/windows/desktop/direct3dtools/iobjecttablecallback)

 

 
