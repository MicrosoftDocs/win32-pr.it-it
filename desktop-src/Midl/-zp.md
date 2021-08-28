---
title: Opzione /Zp
description: L'opzione /Zp è uguale all'opzione /pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- Opzione /Zp MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1795068aae1a5a8c3e793b828d5a80dbab369e16f9c5383af367b66d0febc738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067442"
---
# <a name="zp-switch"></a>Opzione /Zp

**L'opzione /Zp** è uguale all'opzione [**/pack.**](-pack.md)

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*livello di \_ packing* 
</dt> <dd>

Specifica il livello di pacchetto delle strutture nel sistema di destinazione. Il valore a livello di pacchetto può essere impostato su 1, 2, 4 o 8.

</dd> </dl>

## <a name="remarks"></a>Commenti

**L'opzione /Zp** definisce il livello di pacchetto delle strutture nel sistema di destinazione. Il valore a livello di pacchetto corrisponde al **valore dell'opzione /Zp** usato dal compilatore Microsoft C/C++. Per altre informazioni, vedere la documentazione sulla programmazione Microsoft C/C++.

Specificare lo stesso livello di pacchetto quando si richiamano il compilatore MIDL e il compilatore C.

Il livello di pacchetto predefinito usato quando **l'opzione /Zp** o [**/pack**](-pack.md) non è specificata è 8 in tutti gli ambienti di compilazione.

> [!Note]  
> Non usare **/Zp1** o **/Zp2** su piattaforme MIPS o Alpha e **non usare /Zp4** o **/Zp8** su piattaforme a 16 bit. A seconda del tipo di dati e della posizione di memoria assegnati dal compilatore C in fase di esecuzione, ciò può causare un'eccezione di disallineamento dei dati nelle piattaforme MIPS e Alpha. Nelle piattaforme MS-DOS, il compilatore C non garantisce l'allineamento a 4 o 8 e pertanto l'applicazione può terminare.

 

## <a name="examples"></a>Esempio

**midl /Zp4 filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/pack**](-pack.md)
</dt> </dl>

 

 




