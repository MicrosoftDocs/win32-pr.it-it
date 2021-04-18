---
description: La proprietà SOURCE list è un elenco delimitato da punti e virgola di percorsi di origine di rete o URL per il pacchetto di installazione dell'applicazione.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SOURCEs (proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324852"
---
# <a name="sourcelist-property"></a>SOURCEs (proprietà)

La proprietà **source** list è un elenco delimitato da punti e virgola di percorsi di origine di rete o URL per il pacchetto di installazione dell'applicazione. Questo elenco viene aggiunto alla fine dell'elenco di origine di ogni utente esistente per l'applicazione. Il programma di installazione individua un'origine enumerando l'elenco dei percorsi di origine e usa il primo percorso accessibile individuato. Solo questa origine può essere utilizzata per il resto dell'installazione. Ogni percorso specificato nell'elenco di origine deve quindi essere un percorso che disponga di un'origine completa per l'applicazione. L'intero albero di directory in ogni percorso di origine deve essere lo stesso e deve includere tutti i file di origine necessari, inclusi tutti i file CAB. Ogni percorso deve avere un file con estensione msi con lo stesso nome file e il codice prodotto.

## <a name="default-value"></a>Valore predefinito

Il programma di installazione controlla solo la proprietà **SourceName** se il prodotto non è già stato pubblicizzato o installato. In tutti gli altri casi, il programma di installazione usa l'elenco di origine esistente nel registro di sistema.

## <a name="remarks"></a>Commenti

Le origini aggiunte utilizzando la proprietà di **origine** vengono aggiunte direttamente alla fine dell'elenco per ogni tipo di origine e si trovano sempre dopo l'origine predefinita specificata dalla proprietà [**SourceDir**](sourcedir.md) .

Per Windows Installer il numero di origini nella proprietà di **origine** è illimitato. [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) può essere usato per aggiungere origini di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 




