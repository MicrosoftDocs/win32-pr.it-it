---
title: Opzione /server
description: L'opzione /server indica al compilatore MIDL di generare file di origine C sul lato server per un'interfaccia RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /server switch MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf634e9ce91e937ff1e43b9059d12181dc723695139001ec368109d6fdf4a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067471"
---
# <a name="server-switch"></a>Opzione /server

**L'opzione /server** indica al compilatore MIDL di generare file di origine C sul lato server per un'interfaccia RPC.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub****


</dt> <dd>

Genera i file sul lato server.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>none****


</dt> <dd>

Non genera file sul lato server.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Quando **l'opzione /server** non è specificata, il compilatore MIDL genera il file stub del server. Questa opzione non influisce sulle interfacce OLE.

**L'opzione none** causa la generazione di alcun file.

**L'opzione /server** ha la precedenza **sull'opzione /sstub.**

## <a name="examples"></a>Esempio

**midl /server nessuno**

**midl /server stub**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




