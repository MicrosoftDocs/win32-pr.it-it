---
description: La proprietà riepilogo sicurezza indica se il pacchetto deve essere aperto in sola lettura.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Proprietà Riepilogo sicurezza
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331785"
---
# <a name="security-summary-property"></a>Proprietà Riepilogo sicurezza

La proprietà **Riepilogo sicurezza** indica se il pacchetto deve essere aperto in sola lettura. Lo strumento di modifica del database non deve modificare un database applicato di sola lettura e deve generare un avviso in caso di tentativi di modifica di un database consigliato di sola lettura. I seguenti valori di questa proprietà sono applicabili ai file di Windows Installer.



| Valore | Descrizione           |
|-------|-----------------------|
| 0     | Nessuna restrizione        |
| 2     | Di sola lettura consigliata |
| 4     | Applicazione di sola lettura    |



 

Questa proprietà deve essere impostata su sola lettura consigliata (2) per un database di installazione e per l'applicazione di sola lettura (4) per una trasformazione o una patch.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




