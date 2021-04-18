---
description: Il programma di installazione imposta la proprietà VersionNT sul numero di versione del sistema operativo, non definito se il sistema operativo non è Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 o Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Proprietà VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328755"
---
# <a name="versionnt-property"></a>Proprietà VersionNT

Il programma di installazione imposta la proprietà **VersionNT** sul numero di versione del sistema operativo, non definito se il sistema operativo non è Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 o Windows 7. Il valore è un numero intero: MajorVersion \* 100 + MinorVersion.

Questa proprietà può essere utilizzata dalle istruzioni condizionali che dipendono dal sistema operativo.

Vedere anche [valori delle proprietà del sistema operativo](operating-system-property-values.md).

## <a name="remarks"></a>Commenti

Le espressioni di condizione possono eseguire il test per Windows NT, Windows 2000 o Windows XP utilizzando il nome della proprietà oppure possono verificare la versione utilizzando un operatore di confronto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack di Windows minimo richiesto da una versione di Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




