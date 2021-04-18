---
description: La proprietà riepilogo parole chiave nei database o nelle trasformazioni di installazione contiene un elenco di parole chiave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Proprietà di riepilogo parole chiave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330491"
---
# <a name="keywords-summary-property"></a>Proprietà di riepilogo parole chiave

La proprietà **Riepilogo parole chiave** nei database o nelle trasformazioni di installazione contiene un elenco di parole chiave. Le parole chiave possono essere usate dai browser di file per cercare un file. Questa proprietà contiene un elenco di origini della patch in un pacchetto di patch.

Per fornire il valore di questa proprietà nelle informazioni di riepilogo, spetta all'autore di un database di installazione, di una trasformazione o di un pacchetto di patch. Per determinare il valore corretto, gli autori devono eseguire le operazioni seguenti.

-   In un pacchetto di installazione, impostare il valore di questa proprietà su un elenco di parole chiave. La parola chiave deve includere "Installer", nonché parole chiave specifiche del prodotto, e può essere localizzata.
-   In una trasformazione, impostare il valore di questa proprietà su un elenco di parole chiave. La parola chiave deve includere "Installer", nonché parole chiave specifiche del prodotto, e può essere localizzata.
-   In un pacchetto di patch, impostare il valore di questa proprietà su un elenco delimitato da punti e virgola dei percorsi di rete o URL per le origini della patch. Quando la patch viene installata, il programma di installazione li aggiunge all'elenco di origine per il pacchetto di patch. Se la patch memorizzata nella cache risulta mancante, il programma di installazione può cercare un'origine nel percorso originale, un percorso aggiunto all'elenco di origine in base alla proprietà di **Riepilogo delle parole chiave** o un percorso aggiunto all'elenco di origine usando le funzioni [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) o [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




