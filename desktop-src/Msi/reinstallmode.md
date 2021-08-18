---
description: La proprietà REINSTALLMODE è una stringa contenente lettere che specificano il tipo di reinstallazione da eseguire.
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: REINSTALLMODE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 227a069fa0974758bf623c83ef23d40902d9feb140f69446c57c2d723468054f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637877"
---
# <a name="reinstallmode-property"></a>REINSTALLMODE - proprietà

La **proprietà REINSTALLMODE** è una stringa contenente lettere che specificano il tipo di reinstallazione da eseguire. Le opzioni non tra maiuscole e minuscole e indipendenti dall'ordine. Questa proprietà in genere deve essere usata sempre insieme alla [**proprietà REINSTALL.**](reinstall.md) Tuttavia, questa proprietà può essere usata anche durante l'installazione, non solo per la reinstallazione.

> [!Note]  
> Il Windows installer ignora la proprietà **REINSTALLMODE** durante [un'installazione amministrativa.](administrative-installation.md)

 

## <a name="reinstall-option-codes"></a>Codici di opzione di reinstallazione

Per impostazione **predefinita, REINSTALLMODE** è "omus".



| Codice | Opzione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | Reinstallare solo se il file è mancante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | Reinstallare se il file è mancante o è una versione precedente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| h    | Reinstallare se il file è mancante o è una versione uguale o precedente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | Reinstallare se il file è mancante o se è presente una versione diversa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | Verificare i valori di checksum e reinstallare il file se sono mancanti o danneggiati. Questo flag ripristina solo i file con msidbFileAttributesChecksum nella colonna Attributi della [tabella file](file-table.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a    | Forzare la reinstallazione di tutti i file, indipendentemente dal checksum o dalla versione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | Riscrivere tutte le voci del Registro di sistema necessarie dalla tabella del Registro [di](registry-table.md) sistema che passano alla **chiave HKEY CURRENT \_ \_ USER**<br/> o **HKEY \_ USERS**<br/> hive del Registro di sistema.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | Riscrivere tutte le voci del Registro di sistema necessarie dalla tabella del Registro [di](registry-table.md) sistema che passano alla **chiave HKEY LOCAL \_ \_ MACHINE**<br/> o **HKEY \_ CLASSES \_ ROOT**<br/> hive del Registro di sistema. Riscrivere tutte le informazioni dalla tabella class [,](class-table.md)dalla tabella [verbo](verb-table.md), dalla tabella [PublishComponent](publishcomponent-table.md), dalla tabella [ProgID](progid-table.md), dalla tabella [MIME](mime-table.md), [dalla tabella icon](icon-table.md), dalla tabella [extension](extension-table.md)e dalla tabella [AppID](appid-table.md) indipendentemente dall'assegnazione del computer o dell'utente. Reinstallare tutti [**i componenti qualificati.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) Quando si reinstalla un'applicazione, questa opzione esegue le [azioni RegisterTypeLibraries](registertypelibraries-action.md) [e InstallODBC.](installodbc-action.md)<br/> |
| s    | Reinstallare tutti i collegamenti e memorizzare nuovamente nella cache tutte le icone sovrascrivendo eventuali collegamenti e icone esistenti.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | Usare per eseguire dal pacchetto di origine e memorizzare nuovamente nella cache il pacchetto locale. Non usare il codice dell'opzione v reinstall per la prima installazione di un'applicazione o di una funzionalità.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

Se la **proprietà REINSTALLMODE** viene definita senza definire anche la proprietà [**REINSTALL,**](reinstall.md) le modalità di "rilevamento" specificate vengono comunque applicate e viene specificata la modalità di sovrascrittura per un'installazione normale. La **proprietà REINSTALLMODE** influisce solo sulle funzionalità normalmente selezionate per l'installazione. La presenza della proprietà **REINSTALLMODE** non reinstalla le funzionalità. La reinstallazione delle funzionalità richiede la presenza della **proprietà REINSTALL.**

I codici di opzione per questa proprietà corrispondono all'opzione della [riga di comando](command-line-options.md) '/f'. L'opzione della riga di comando ha un valore predefinito "pecms".

> [!Note]  
> Solo i file contenenti informazioni sul checksum vengono mai verificati e ripristinati. Il flag REINSTALLMODE FILEVERIFY (il codice ccode precedente) ripristina solo i file con \_ msidbFileAttributesChecksum nella colonna Attributi della [tabella file](file-table.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




