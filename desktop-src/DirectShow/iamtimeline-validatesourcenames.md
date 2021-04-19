---
description: Il metodo ValidateSourceNames convalida i nomi di origine nella sequenza temporale, usando il localizzatore multimediale. Facoltativamente, questo metodo aggiorna anche tutti gli oggetti di origine per i quali individua un file.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'Metodo IAMTimeline:: ValidateSourceNames (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330186"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>Metodo IAMTimeline:: ValidateSourceNames

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `ValidateSourceNames` metodo convalida i nomi di origine nella sequenza temporale, usando il localizzatore multimediale. Facoltativamente, questo metodo aggiorna anche tutti gli oggetti di origine per i quali individua un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ValidateFlags* 
</dt> <dd>

Combinazione bit per bit dei [**flag di convalida dei nomi di file**](file-name-validation-flags.md) che specificano il comportamento del localizzatore multimediale. I \_ flag di controllo SFN VALIDATEF \_ Replace e SFN \_ VALIDATEF \_ devono essere presenti oppure il metodo restituisce e \_ INVALIDARG.

</dd> <dt>

*pOverride* 
</dt> <dd>

Puntatore facoltativo all'interfaccia [**IMediaLocator**](imedialocator.md) di un localizzatore multimediale da usare al posto del valore predefinito. Per usare il localizzatore multimediale predefinito, impostare il valore di questo parametro su **null**. Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*NotifyEventHandle* 
</dt> <dd>

Handle per un evento. Il metodo segnala l'evento dopo aver completato la convalida.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Utilizzando il parametro *pOverride* , è possibile fornire un'implementazione personalizzata dell'interfaccia [**IMediaLocator**](imedialocator.md) . Ad esempio, il localizzatore multimediale predefinito non invierà una notifica all'applicazione sui file che trova (o non è in grado di trovare). Per aggirare questa limitazione, è possibile implementare un localizzatore multimediale personalizzato, rendendolo un wrapper per la versione predefinita. Nella versione personalizzata passare [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) chiamate direttamente alla versione predefinita ed esaminare il valore restituito.

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

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




