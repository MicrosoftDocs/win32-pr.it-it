---
description: Il programma di installazione imposta la proprietà MsiNTProductType per i sistemi operativi Windows NT, Windows 2000 e versioni successive.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Proprietà MsiNTProductType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330149"
---
# <a name="msintproducttype-property"></a>Proprietà MsiNTProductType

Il programma di installazione imposta la proprietà **MsiNTProductType** per i sistemi operativi Windows NT, Windows 2000 e versioni successive. Questa proprietà indica il tipo di prodotto Windows.

Per i sistemi operativi Windows 2000 e versioni successive, il programma di installazione imposta i valori seguenti. Si noti che i valori corrispondono a quelli del campo **wProductType** della struttura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .



| Valore | Significato                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional e versioni successive      |
| 2     | Controller di dominio Windows 2000 e versioni successive |
| 3     | Windows 2000 Server e versioni successive            |



 

Per i sistemi operativi precedenti a Windows 2000, il programma di installazione imposta i valori seguenti.



| Valore | Significato                      |
|-------|------------------------------|
| 1     | Workstation Windows NT       |
| 2     | Controller di dominio Windows NT |
| 3     | Windows NT Server            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
