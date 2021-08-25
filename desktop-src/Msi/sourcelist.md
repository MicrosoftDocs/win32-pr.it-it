---
description: La proprietà SOURCELIST è un elenco delimitato da punto e virgola di percorsi di origine url o di rete per il pacchetto di installazione dell'applicazione.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SOURCELIST - proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd0ab879d55481f71c663e4375a305232be576d0c923f67fa419530012d1ce89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893751"
---
# <a name="sourcelist-property"></a>SOURCELIST - proprietà

La **proprietà SOURCELIST** è un elenco delimitato da punto e virgola di percorsi di origine url o di rete per il pacchetto di installazione dell'applicazione. Questo elenco viene aggiunto alla fine dell'elenco di origine esistente di ogni utente per l'applicazione. Il programma di installazione individua un'origine enumerando l'elenco dei percorsi di origine e usa il primo percorso accessibile trovato. Solo questa origine può essere usata per il resto dell'installazione. Ogni percorso specificato nell'elenco di origine deve quindi essere in un percorso con un'origine completa per l'applicazione. L'intero albero di directory in ogni percorso di origine deve essere lo stesso e deve includere tutti i file di origine necessari, inclusi gli eventuali file cab. Ogni percorso deve avere un .msi file con lo stesso nome file e lo stesso codice prodotto.

## <a name="default-value"></a>Valore predefinito

Il programma di installazione controlla la **proprietà SOURCELIST** solo se il prodotto non è già stato annunciato o installato. In tutti gli altri casi il programma di installazione usa l'elenco di origine esistente presente nel Registro di sistema.

## <a name="remarks"></a>Commenti

Le origini aggiunte tramite la proprietà **SOURCELIST** vengono aggiunte direttamente alla fine dell'elenco per ogni tipo di origine e vengono sempre dopo l'origine predefinita specificata dalla [**proprietà SourceDir.**](sourcedir.md)

Ad Windows programma di installazione il numero di origini nella **proprietà SOURCELIST** è illimitato. [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) può essere usato per aggiungere origini di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Resilienza dell'origine](source-resiliency.md)
</dt> </dl>

 

 




