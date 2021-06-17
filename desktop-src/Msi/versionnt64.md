---
description: Il programma di installazione imposta la proprietà VersionNT64 sul numero di versione del sistema operativo solo se il sistema è in esecuzione in un computer a 64 bit.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64 - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262073"
---
# <a name="versionnt64-property"></a>VersionNT64 - proprietà

Il programma di installazione **imposta la proprietà VersionNT64** sul numero di versione del sistema operativo solo se il sistema è in esecuzione in un computer a 64 bit. La proprietà non è definita se il sistema operativo non è a 64 bit.

Il valore è un numero intero: MajorVersion \* 100 + MinorVersion.

Per motivi di compatibilità, la [](template-summary.md) proprietà non è definita anche se la proprietà Riepilogo modello indica che il pacchetto è per sistemi Intel (x86) a 32 bit e il sistema operativo non può eseguire codice Intel (x64) a 64 bit, ad esempio Windows 10 on ARM (ARM64).

> [!NOTE]
> A Windows 10 build 21277, le build ARM64 nel canale Dev del programma Windows Insider Preview supportano le applicazioni x64. In queste build ARM64 la proprietà VersionNT64 è definita per i pacchetti x86.

## <a name="remarks"></a>Commenti

Le espressioni condizionali eseguono il test per Windows a 64 bit semplicemente usando il nome della proprietà o verificando la versione usando un operatore di confronto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5.0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP Vedere i requisiti [di Windows Installer Run-Time](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una Windows Installer versione.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




