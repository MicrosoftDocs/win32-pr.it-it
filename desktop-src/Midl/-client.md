---
title: opzione/client
description: L'opzione/client indica al compilatore MIDL di generare file di origine C sul lato client per un'interfaccia RPC.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /client switch MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334575"
---
# <a name="client-switch"></a>opzione/client

L'opzione **/client** indica al compilatore MIDL di generare file di origine C sul lato client per un'interfaccia RPC.

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>Stub * * * *


</dt> <dd>

Genera i file sul lato client.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>nessuno * * * *


</dt> <dd>

Non genera alcun file lato client.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Quando l'opzione **/client** non è specificata, il compilatore MIDL genera il file stub del client. Questa opzione non influisce sulle interfacce OLE.

L'opzione **/client** ha la precedenza sull'opzione [**/cstub**](-cstub.md) .

## <a name="examples"></a>Esempio

**MIDL/client None nomefile. idl**

**nome file stub MIDL/client. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Server**](-server.md)
</dt> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




