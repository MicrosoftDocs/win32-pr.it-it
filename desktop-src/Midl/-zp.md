---
title: Opzione/Zp
description: L'opzione/Zp è uguale all'opzione/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /ZP switch MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718160"
---
# <a name="zp-switch"></a>Opzione/Zp

L'opzione **/ZP** è uguale all'opzione [**/Pack**](-pack.md) .

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*livello di compressione \_* 
</dt> <dd>

Specifica il livello di compressione delle strutture nel sistema di destinazione. Il valore a livello di compressione può essere impostato su 1, 2, 4 o 8.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'opzione **/ZP** designa il livello di compressione delle strutture nel sistema di destinazione. Il valore a livello di compressione corrisponde al valore dell'opzione **/ZP** usato dal compilatore Microsoft C/C++. Per ulteriori informazioni, vedere la documentazione sulla programmazione in Microsoft C/C++.

Specificare lo stesso livello di compressione quando si richiama il compilatore MIDL e il compilatore C.

Il livello di compressione predefinito utilizzato quando non viene specificata né l'opzione **/ZP** né [**/Pack**](-pack.md) è 8 in tutti gli ambienti di compilazione.

> [!Note]  
> Non usare **/Zp1** o **/ZP2** su piattaforme MIPS o Alpha e non usare **/zp4** o **/ZP8** su piattaforme a 16 bit. A seconda del tipo di dati e della posizione di memoria assegnati dal compilatore C in fase di esecuzione, può verificarsi un'eccezione di allineamento dei dati sulle piattaforme MIPS e Alpha. Sulle piattaforme MS-DOS, il compilatore C non assicurerà l'allineamento a 4 o 8, quindi l'applicazione potrebbe terminare.

 

## <a name="examples"></a>Esempio

**MIDL/zp4 nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> </dl>

 

 




