---
description: Il metodo WriteGrfFile scrive un grafico di filtro in un file in formato GRF.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'Metodo IXml2Dex:: WriteGrfFile (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328454"
---
# <a name="ixml2dexwritegrffile-method"></a>Metodo IXml2Dex:: WriteGrfFile

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `WriteGrfFile` metodo scrive un grafico di filtro in un file in formato. GRF.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGraph* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** del grafico dei filtri.

</dd> <dt>

*FileName* 
</dt> <dd>

Stringa che specifica il nome del file da scrivere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** che dipende dall'implementazione dell'interfaccia. HRESULT può includere una delle seguenti costanti standard o altri valori non elencati.



| Codice restituito                                                                                  | Descrizione                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ non riescono**</dt> </dl>       | Esito negativo.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argomento non valido.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>             |



 

Questo metodo può inoltre restituire i codici di errore generati dalle chiamate interne ai metodi **IStorage:: CreateStream** e **IPersist:: Save** . Per ulteriori informazioni, vedere Platform SDK.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Internet Explorer 4,0 o versione successiva<br/>                                               |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




