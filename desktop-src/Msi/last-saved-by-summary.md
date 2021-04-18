---
description: Il programma di installazione imposta l'ultima proprietà salvata da riepilogo su un valore che dipende dal fatto che si tratti di un pacchetto di installazione, una trasformazione o un pacchetto di patch. In un pacchetto di installazione, il programma di installazione imposta questa proprietà sul valore della proprietà LogonUser durante un'installazione amministrativa. Gli sviluppatori di strumenti di modifica del database possono utilizzare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che ha modificato il database di installazione. Questa proprietà deve essere impostata su null in un database di spedizione finale. Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla. In una trasformazione questa proprietà di riepilogo contiene gli ID della piattaforma e della lingua che un database deve avere dopo che è stato trasformato. La proprietà specifica l'elemento che deve essere impostato nel riepilogo del modello nel nuovo database. In un pacchetto di patch questa proprietà di riepilogo contiene un elenco delimitato da punti e virgola di nomi di sottoarchivi di trasformazione nell'ordine in cui sono applicati da questa patch.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Ultimo salvataggio da proprietà di riepilogo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330488"
---
# <a name="last-saved-by-summary-property"></a>Ultimo salvataggio da proprietà di riepilogo

Il programma di installazione imposta l' **ultima proprietà salvata da riepilogo** su un valore che dipende dal fatto che si tratti di un pacchetto di installazione, una trasformazione o un pacchetto di patch.

In un pacchetto di installazione, il programma di installazione imposta questa proprietà sul valore della proprietà [**LogonUser**](logonuser.md) durante un' [installazione amministrativa](administrative-installation.md). Gli sviluppatori di strumenti di modifica del database possono utilizzare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che ha modificato il database di installazione. Questa proprietà deve essere impostata su null in un database di spedizione finale. Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla.

In una trasformazione questa proprietà di riepilogo contiene gli ID della piattaforma e della lingua che un database deve avere dopo che è stato trasformato. La proprietà specifica l'elemento che deve essere impostato nel [**Riepilogo del modello**](template-summary.md) nel nuovo database.

In un pacchetto di patch questa proprietà di riepilogo contiene un elenco delimitato da punti e virgola di nomi di sottoarchivi di trasformazione nell'ordine in cui sono applicati da questa patch.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




