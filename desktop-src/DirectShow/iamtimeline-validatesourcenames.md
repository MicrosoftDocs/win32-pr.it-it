---
description: Il metodo ValidateSourceNames convalida i nomi di origine nella sequenza temporale usando il localizzatore multimediale. Facoltativamente, questo metodo aggiorna anche qualsiasi oggetto di origine per il quale individua un file.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: Metodo IAMTimeline::ValidateSourceNames (Qedit.h)
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
ms.openlocfilehash: cabaa5f9ec67abaf8805ad55917d0a33b6ad3457bedd8899b3f443f1a247b8d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043111"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>Metodo IAMTimeline::ValidateSourceNames

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `ValidateSourceNames` metodo convalida i nomi di origine nella sequenza temporale usando il localizzatore multimediale. Facoltativamente, questo metodo aggiorna anche qualsiasi oggetto di origine per il quale individua un file.

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

Combinazione bit per bit [**dei flag di convalida dei**](file-name-validation-flags.md) nomi file che specificano il comportamento del localizzatore multimediale. I flag SFN VALIDATEF REPLACE e \_ \_ SFN VALIDATEF CHECK devono essere presenti oppure il metodo restituisce \_ \_ E \_ INVALIDARG.

</dd> <dt>

*pOverride* 
</dt> <dd>

Puntatore facoltativo [**all'interfaccia IMediaLocator**](imedialocator.md) di un localizzatore multimediale da usare al posto dell'impostazione predefinita. Per usare il localizzatore multimediale predefinito, impostare il valore di questo parametro su **NULL.** Per ulteriori informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*NotifyEventHandle* 
</dt> <dd>

Handle per un evento. Il metodo segnala l'evento dopo aver completato la convalida.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Usando il *parametro pOverride,* è possibile fornire un'implementazione personalizzata dell'interfaccia [**IMediaLocator.**](imedialocator.md) Ad esempio, il localizzatore multimediale predefinito non invierà una notifica all'applicazione sui file trovati (o non trovati). Per aggirare questa limitazione, è possibile implementare un localizzatore multimediale personalizzato, rendendolo un wrapper per la versione predefinita. Nella versione personalizzata passare [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) chiama direttamente la versione predefinita ed esaminare il valore restituito.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




