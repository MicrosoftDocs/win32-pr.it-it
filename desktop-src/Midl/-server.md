---
title: parametro/Server
description: Il parametro/Server indica al compilatore MIDL di generare file di origine C sul lato server per un'interfaccia RPC.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /server-switch MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045758"
---
# <a name="server-switch"></a>parametro/Server

Il parametro **/Server** indica al compilatore MIDL di generare file di origine C sul lato server per un'interfaccia RPC.

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>Stub * * * *


</dt> <dd>

Genera i file sul lato server.

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>nessuno * * * *


</dt> <dd>

Non genera file sul lato server.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Se non si specifica l'opzione **/Server** , il compilatore MIDL genera il file stub del server. Questa opzione non influisce sulle interfacce OLE.

L'opzione **None** non comporta la generazione di file.

L'opzione **/Server** ha la precedenza sull'opzione **/sstub**

## <a name="examples"></a>Esempio

**non MIDL, nessuno**

**Stub di MIDL/server**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




