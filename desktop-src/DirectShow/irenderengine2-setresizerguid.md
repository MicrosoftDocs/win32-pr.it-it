---
description: Il metodo SetResizerGUID specifica il CLSID di un filtro di ridimensionamento video personalizzato.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'Metodo IRenderEngine2:: SetResizerGUID (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332575"
---
# <a name="irenderengine2setresizerguid-method"></a>Metodo IRenderEngine2:: SetResizerGUID

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetResizerGUID` metodo specifica il CLSID di un filtro di ridimensionamento video personalizzato. Chiamare questo metodo per sostituire il filtro di ridimensionamento predefinito utilizzato dai servizi di modifica DirectShow. Il filtro deve essere registrato come oggetto COM nel sistema dell'utente e deve supportare l'interfaccia [**IResize**](iresize.md) .

Chiamare questo metodo prima di chiamare [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ResizerGuid* \[ in\]
</dt> <dd>

CLSID del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Per ripristinare il valore predefinito DES Resizer, usare il CLSID seguente:


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9,0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IRenderEngine2**](irenderengine2.md)
</dt> </dl>

 

 




