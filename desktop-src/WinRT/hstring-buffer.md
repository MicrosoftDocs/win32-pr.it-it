---
description: Handle per un buffer di stringa modificabile che è possibile utilizzare per creare un HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (HSTRING. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307082"
---
# <a name="hstring_buffer"></a>\_buffer HString

Handle per un buffer di stringa modificabile che è possibile utilizzare per creare un [**HString**](hstring.md).


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Commenti

**HString \_ Il BUFFER** rappresenta un buffer di stringa che è possibile modificare prima di convertirlo in un [**HString**](hstring.md)non modificabile.

Chiamare la funzione [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) per creare un **\_ buffer HString**. Chiamare [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) per convertire un **\_ buffer HString** in un [**HString**](hstring.md)non modificabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>HSTRING. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
