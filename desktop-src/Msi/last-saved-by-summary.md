---
description: Il programma di installazione imposta la proprietà Ultimo salvataggio per riepilogo su un valore che dipende dal fatto che si tratta di un pacchetto di installazione, di una trasformazione o di un pacchetto patch. In un pacchetto di installazione, il programma di installazione imposta questa proprietà sul valore della proprietà LogonUser durante un'installazione amministrativa. Gli sviluppatori di strumenti di modifica del database possono usare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che modifica il database di installazione. Questa proprietà deve essere impostata su Null in un database di spedizione finale. Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla. In una trasformazione questa proprietà di riepilogo contiene gli ID piattaforma e lingua che un database deve avere dopo la trasformazione. La proprietà specifica l'impostazione di Riepilogo modelli nel nuovo database. In un pacchetto patch, questa proprietà di riepilogo contiene un elenco delimitato da punto e virgola di nomi di sottostorage di trasformazione nell'ordine in cui vengono applicati da questa patch.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Last Saved By Summary - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9299dc6a00af4e48eb3901842aba58a3c8d9a9c1d98d3a3e1e0f05bfccc4333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979451"
---
# <a name="last-saved-by-summary-property"></a>Last Saved By Summary - proprietà

Il programma di installazione imposta **la proprietà** Ultimo salvataggio per riepilogo su un valore che dipende dal fatto che si tratta di un pacchetto di installazione, di una trasformazione o di un pacchetto patch.

In un pacchetto di installazione, il programma di installazione imposta questa proprietà sul valore della [**proprietà LogonUser**](logonuser.md) durante un'installazione [amministrativa.](administrative-installation.md) Gli sviluppatori di strumenti di modifica del database possono usare questa proprietà durante il processo di sviluppo per tenere traccia dell'ultima persona che modifica il database di installazione. Questa proprietà deve essere impostata su Null in un database di spedizione finale. Il programma di installazione non usa mai questa proprietà e un utente non deve mai modificarla.

In una trasformazione questa proprietà di riepilogo contiene gli ID piattaforma e lingua che un database deve avere dopo la trasformazione. La proprietà specifica l'impostazione [**di Riepilogo**](template-summary.md) modelli nel nuovo database.

In un pacchetto patch, questa proprietà di riepilogo contiene un elenco delimitato da punto e virgola di nomi di sottostorage di trasformazione nell'ordine in cui vengono applicati da questa patch.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




