---
description: La proprietà Riepilogo parole chiave nei database di installazione o nelle trasformazioni contiene un elenco di parole chiave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Proprietà Riepilogo parole chiave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a572161e440b440010d43f598e2baa453dbca514d71aa6f0f672deb7c726fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680311"
---
# <a name="keywords-summary-property"></a>Proprietà Riepilogo parole chiave

La **proprietà Riepilogo parole** chiave nei database di installazione o nelle trasformazioni contiene un elenco di parole chiave. Le parole chiave possono essere usate dai browser di file per eseguire ricerche di parole chiave per un file. Questa proprietà contiene un elenco di origini della patch in un pacchetto di patch.

L'autore di un database di installazione, una trasformazione o un pacchetto patch deve fornire il valore di questa proprietà nelle informazioni di riepilogo. Gli autori devono eseguire le operazioni seguenti per determinare il valore corretto.

-   In un pacchetto di installazione impostare il valore di questa proprietà su un elenco di parole chiave. La parola chiave deve includere "Installer" e parole chiave specifiche del prodotto e può essere localizzata.
-   In una trasformazione impostare il valore di questa proprietà su un elenco di parole chiave. La parola chiave deve includere "Installer" e parole chiave specifiche del prodotto e può essere localizzata.
-   In un pacchetto patch impostare il valore di questa proprietà su un elenco delimitato da punto e virgola di percorsi di rete o URL per le origini della patch. Quando la patch viene installata, il programma di installazione li aggiunge all'elenco di origine per il pacchetto di patch. Se la patch memorizzata nella cache risulta mancante, il programma di installazione può  cercare un'origine nel percorso originale, un percorso aggiunto all'elenco di origine dalla proprietà Riepilogo parole chiave o un percorso aggiunto all'elenco di origine usando le funzioni [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) o [**MsiSourceListAddSourceEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




