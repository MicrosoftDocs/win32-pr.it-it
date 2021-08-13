---
title: IWMPDVD.isAvailable (VB e C )
description: La proprietà isAvailable (il metodo get isAvailable in C\ ) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire \_ un'azione specificata.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD.isAvailable (VB e C ) Windows Media Player
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
ms.openlocfilehash: c78c9dda7bff764752dc55524000ccd3695863afe69dcf45c2ed971c9c0373fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415921"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>IWMPDVD.isAvailable (VB e C#)

La **proprietà isAvailable** (metodo **get \_ isAvailable** in C#) ottiene un valore che indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.


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

Oggetto System.String che è uno dei valori seguenti.



| Valore      | Descrizione                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| Indietro       | Individua se il **metodo IWMPDVD.back** è disponibile.                                   |
| Dvd        | Individua se il DVD è caricato.                                                          |
| dvdDecoder | Individua se il decodificatore DVD è installato nel sistema.                                     |
| resume     | Individua se il **metodo IWMPDVD.resume** è disponibile.                                 |
| titleMenu  | Individua se il **metodo IWMPDVD.titleMenu** è disponibile.                              |
| topMenu    | Individua se il **metodo IWMPDVD.topMenu** è disponibile. Comunemente chiamato menu radice. |



 

## <a name="property-value"></a>Valore della proprietà

**System.Boolean**

Valore **System.Boolean che** indica se è disponibile un tipo specificato di informazioni o se è possibile eseguire un'azione specificata.

## <a name="remarks"></a>Commenti

Le funzionalità DVD Windows Media Player non funzionano nei computer in cui non è installato un decodificatore DVD. È possibile determinare se un decodificatore è disponibile chiamando la proprietà **isAvailable** (metodo **get \_ isAvailable** in C#) e passando il valore **System.String** "dvdDecoder".

Ogni DVD viene creato in modo diverso. I metodi disponibili durante la riproduzione e la navigazione dei DVD dipendono dalla modalità di creazione del DVD.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.back (VB e C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.resume (VB e C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.titleMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.topMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





