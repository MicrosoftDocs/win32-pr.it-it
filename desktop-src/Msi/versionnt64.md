---
description: Il programma di installazione imposta la proprietà VersionNT64 sul numero di versione per il sistema operativo solo se il sistema è in esecuzione in un computer a 64 bit.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Proprietà VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326898"
---
# <a name="versionnt64-property"></a>Proprietà VersionNT64

Il programma di installazione imposta la proprietà **VersionNT64** sul numero di versione per il sistema operativo solo se il sistema è in esecuzione in un computer a 64 bit. La proprietà non è definita se il sistema operativo non è a 64 bit.

Il valore è un numero intero: MajorVersion \* 100 + MinorVersion.

Per motivi di compatibilità, anche la proprietà non è definita se la proprietà di [**Riepilogo del modello**](template-summary.md) indica che il pacchetto è per i sistemi Intel a 32 bit e il sistema operativo è un'architettura a 64 bit che non è Intel64 o x64, ad esempio arm64.

## <a name="remarks"></a>Commenti

Le espressioni condizionali testano le finestre a 64 bit semplicemente utilizzando il nome della proprietà o verificando la versione utilizzando un operatore di confronto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP, vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack di Windows minimo richiesto da una versione di Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




