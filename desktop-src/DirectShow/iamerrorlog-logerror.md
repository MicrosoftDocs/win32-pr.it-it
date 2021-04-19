---
description: Il Metodo LogError registra un errore. Le applicazioni non devono chiamare questo metodo. Viene chiamato internamente in risposta agli errori di rendering.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'Metodo IAMErrorLog:: LogError (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326822"
---
# <a name="iamerrorloglogerror-method"></a>Metodo IAMErrorLog:: LogError

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il metodo **LogError** registra un errore. Le applicazioni non devono chiamare questo metodo. Viene chiamato internamente in risposta agli errori di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gravità* 
</dt> <dd>

Riservato. Non usare.

</dd> <dt>

*ErrorString* 
</dt> <dd>

Valore stringa contenente il testo dell'errore.

</dd> <dt>

*ErrorCode* 
</dt> <dd>

Codice di errore.

</dd> <dt>

*HRESULT* 
</dt> <dd>

Valore HRESULT restituito dalla chiamata al metodo che ha causato l'errore.

</dd> <dt>

*pExtraInfo* \[ in\]
</dt> <dd>

Puntatore a una variante che contiene informazioni aggiuntive sull'errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore del parametro *HRESULT* .

## <a name="remarks"></a>Commenti

All'interno di questo metodo, non liberare il **Variant** a cui punta *pExtraInfo*. Inoltre, la **variante** diventa non valida dopo la restituzione del metodo, pertanto non tentare di farvi riferimento in un secondo momento.

Implementare questo metodo per restituire il più rapidamente possibile. Non eseguire chiamate di funzione dall'interno di questo metodo che potrebbero bloccare l'esecuzione del programma. Ad esempio, non chiamare funzioni che inviano messaggi della finestra, bloccano gli eventi o altrimenti potrebbero bloccare l'esecuzione. Questa operazione potrebbe causare l'interruzione della risposta del computer.

Per un elenco degli errori definiti da DES, oltre al significato e al tipo di dati della **variante** a cui punta *PExtraInfo*, vedere [errori di rendering](rendering-errors.md).

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMErrorLog**](iamerrorlog.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




