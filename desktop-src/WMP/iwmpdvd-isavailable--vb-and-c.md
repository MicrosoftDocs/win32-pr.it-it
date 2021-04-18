---
title: IWMPDVD. disavailable (VB e C)
description: La proprietà disavailable (il \_ metodo Get disavailable in C \) ottiene un valore che indica se un tipo specificato di informazioni è disponibile o se è possibile eseguire un'azione specificata.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. disavailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330727"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>IWMPDVD. disavailable (VB e C#)

La **proprietà IsValid (il** metodo **get \_ disavailable** in C#) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a>Parametri

*bstrItem*

System. String che corrisponde a uno dei valori seguenti.



| Valore      | Descrizione                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| Indietro       | Individua se è disponibile il metodo **IWMPDVD. back** .                                   |
| DVD        | Rileva se il DVD è caricato.                                                          |
| dvdDecoder | Rileva se il decoder DVD è installato nel sistema.                                     |
| resume     | Rileva se il metodo **IWMPDVD. Resume** è disponibile.                                 |
| titleMenu  | Rileva se il metodo **IWMPDVD. titleMenu** è disponibile.                              |
| Menu di scelta rapida    | Rileva se il metodo **IWMPDVD. tomenu** è disponibile. Comunemente chiamato menu radice. |



 

## <a name="property-value"></a>Valore della proprietà

**System.Boolean**

**System. Boolean** che indica se un tipo specificato di informazioni è disponibile o se è possibile eseguire un'azione specificata.

## <a name="remarks"></a>Commenti

Le funzionalità DVD di Windows Media Player non funzioneranno nei computer in cui non è installato un decoder DVD. È possibile determinare se un decodificatore è disponibile chiamando la proprietà **disavailable** (il metodo **get \_ disavailable** in C#) e passando il valore **System. String** "dvdDecoder".

Ogni DVD viene creato in modo diverso. I metodi disponibili durante la riproduzione e la navigazione in DVD dipendono dal modo in cui viene creato il DVD.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. Back (VB e C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. Resume (VB e C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. tomenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





