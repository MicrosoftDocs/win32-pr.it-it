---
description: Per ottenere guid del provider o GUID della classe di traccia eventi, è possibile usare lo strumento Uuidgen.exe o Guidgen.exe eventi.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Recupero di un PROVIDER e di un GUID di classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c480a45a5a826d3f258ab267e39db87bc85fad799fef5d7397a7c900f4872f22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914351"
---
# <a name="obtaining-a-provider-and-class-guid"></a>Recupero di un PROVIDER e di un GUID di classe

Per ottenere guid del provider o GUID della classe di traccia eventi, è possibile usare lo strumento Uuidgen.exe o Guidgen.exe eventi.

Se si usa lo strumento Uuidgen.exe, usare l'opzione -d per creare una macro DEFINE GUID C, come \_ illustrato nell'esempio seguente. Per informazioni sull'uso dello Uuidgen.exe, usare il comando -? opzione. Se si usa la macro DEFINE GUID C per definire il GUID, è necessario includere define INITGUID prima delle definizioni GUID, come illustrato \_ \# nell'esempio seguente.

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

Microsoft Windows Software Development Kit (SDK) e Microsoft Visual Studio lo strumento Guidgen.exe. Lo Guidgen.exe dispone di un'interfaccia utente che consente di scegliere tra diversi formati. È consigliabile usare il formato che crea un GUID costante statico, come illustrato nell'esempio seguente.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



