---
description: Il programma di installazione imposta la proprietà MsiNTProductType per Windows NT, Windows 2000 e sistemi operativi successivi.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: MsiNTProductType - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e4c5083e5d1f0195e2e8a8e0cc46213853cb5cf1431535afee7e5362ff5eda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082821"
---
# <a name="msintproducttype-property"></a>MsiNTProductType - proprietà

Il programma di installazione imposta la **proprietà MsiNTProductType** per Windows NT, Windows 2000 e versioni successive. Questa proprietà indica il tipo Windows prodotto.

Per Windows 2000 e versioni successive, il programma di installazione imposta i valori seguenti. Si noti che i valori sono gli stessi del **campo wProductType** della [**struttura OSVERSIONINFOEX.**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)



| Valore | Significato                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional e versioni successive      |
| 2     | Windows 2000 domain controller e versioni successive |
| 3     | Windows 2000 Server e versioni successive            |



 

Per i sistemi operativi precedenti Windows 2000, il programma di installazione imposta i valori seguenti.



| Valore | Significato                      |
|-------|------------------------------|
| 1     | Windows NT Workstation       |
| 2     | Windows NT controller di dominio |
| 3     | Windows NT Server            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
