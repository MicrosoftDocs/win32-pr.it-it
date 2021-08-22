---
description: Il metodo WriteXMLFile converte una sequenza temporale in XML e scrive i dati XML in un file.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: Metodo IXml2Dex::WriteXMLFile (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 81cb33222988b99b9484226e72110afc3eca1923441479adc8d600e2b80f273c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767011"
---
# <a name="ixml2dexwritexmlfile-method"></a>Metodo IXml2Dex::WriteXMLFile

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `WriteXMLFile` metodo converte una sequenza temporale in XML e scrive i dati XML in un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pTimeline* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown dell'oggetto sequenza** temporale.

</dd> <dt>

*FileName* 
</dt> <dd>

Stringa che specifica il nome del file da scrivere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT** che dipende dall'implementazione dell'interfaccia . HRESULT **può** includere una delle costanti standard seguenti o altri valori non elencati.



| Codice restituito                                                                                   | Descrizione                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argomento non valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata.<br/>             |



 

## <a name="remarks"></a>Commenti

Questo metodo genera un file XML che rappresenta tutti i componenti nella sequenza temporale.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Internet Explorer 4.0 o versione successiva<br/>                                               |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




