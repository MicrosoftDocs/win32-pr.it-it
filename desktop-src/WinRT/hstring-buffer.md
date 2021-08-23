---
description: Handle per un buffer di stringa modificabile che è possibile usare per creare un oggetto HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (Hstring.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f115ca18b4bf5b81bbd7004259aa525517c05a3adc0f6376f7d16df3e3ce679
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733821"
---
# <a name="hstring_buffer"></a>HSTRING \_ BUFFER

Handle per un buffer di stringa modificabile che è possibile usare per creare un [**oggetto HSTRING.**](hstring.md)


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Commenti

**HSTRING \_ BUFFER** rappresenta un buffer di stringa che è possibile modificare prima di convertirlo in una [**HSTRING non modificabile.**](hstring.md)

Chiamare la [**funzione WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) per creare **un buffer HSTRING \_**. Chiamare [**WindowsPromoteStringBuffer per**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) convertire **un buffer HSTRING \_** in un [**HSTRING non modificabile.**](hstring.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Hstring.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
