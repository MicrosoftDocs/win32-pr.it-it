---
title: Opzione /client
description: L'opzione /client indica al compilatore MIDL di generare file di origine C sul lato client per un'interfaccia RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- Opzione /client MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8361a41aa0e7c87c42eb41508fee0973d6fd4dd821e2008aa2148c8460fc63ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764361"
---
# <a name="client-switch"></a>Opzione /client

**L'opzione /client** indica al compilatore MIDL di generare file di origine C sul lato client per un'interfaccia RPC.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub****


</dt> <dd>

Genera i file sul lato client.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none****


</dt> <dd>

Non genera file sul lato client.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Quando **l'opzione /client** non è specificata, il compilatore MIDL genera il file stub client. Questa opzione non influisce sulle interfacce OLE.

**L'opzione /client** ha la precedenza [**sull'opzione /cstub.**](-cstub.md)

## <a name="examples"></a>Esempio

**midl /client none filename.idl**

**midl /client stub filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/server**](-server.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




