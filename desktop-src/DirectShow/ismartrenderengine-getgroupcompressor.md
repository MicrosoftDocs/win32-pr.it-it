---
description: Il metodo GetGroupCompressor Recupera il filtro di compressione per il gruppo specificato.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'Metodo ISmartRenderEngine:: GetGroupCompressor (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328610"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>Metodo ISmartRenderEngine:: GetGroupCompressor

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetGroupCompressor` metodo recupera il filtro di compressione per il gruppo specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Gruppo* 
</dt> <dd>

Indice in base zero del gruppo.

</dd> <dt>

*pCompressor* 
</dt> <dd>

Riceve un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di compressione. Riceve il valore **null** se non è presente alcun filtro di compressione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Utilizzare questo metodo per impostare le proprietà sul filtro di compressione, ad esempio la frequenza dei fotogrammi chiave. Chiamare questo metodo dopo la chiamata a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md), ma prima di eseguire il rendering del progetto. Eseguire quindi una query sul pin di output del filtro di compressione per l'interfaccia [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , che contiene i metodi per l'impostazione dei parametri di compressione. Al termine, rilasciare l'interfaccia. Se si apportano modifiche successive alla sequenza temporale, chiamare **ConnectFrontEnd**, quindi chiamare di nuovo **GetGroupCompressor** per reimpostare i parametri di compressione.

In caso di restituzione, se il valore di \* *pCompressor* è diverso da **null**, l'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) include un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

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

[**Interfaccia ISmartRenderEngine**](ismartrenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




