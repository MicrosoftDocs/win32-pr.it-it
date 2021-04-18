---
description: La proprietà REINSTALLMODE è una stringa che contiene lettere che specificano il tipo di reinstallazione da eseguire.
ms.assetid: 756d2899-2cfe-473a-bebf-a7f7bbe7d229
title: Proprietà REINSTALLMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab48043ef92770cbc3a1f5ab92e459128c9945ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328552"
---
# <a name="reinstallmode-property"></a>Proprietà REINSTALLMODE

La proprietà **REINSTALLMODE** è una stringa che contiene lettere che specificano il tipo di reinstallazione da eseguire. Le opzioni non fanno distinzione tra maiuscole e minuscole e indipendenti dagli ordini. Questa proprietà in genere deve essere sempre utilizzata insieme alla proprietà [**REINSTALL**](reinstall.md) . Tuttavia, questa proprietà può essere usata anche durante l'installazione, non solo reinstallare.

> [!Note]  
> Il Windows Installer ignora la proprietà **REINSTALLMODE** durante un' [installazione amministrativa](administrative-installation.md).

 

## <a name="reinstall-option-codes"></a>Reinstallare i codici delle opzioni

Per impostazione predefinita, **REINSTALLMODE** è "omus".



| Codice | Opzione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| p    | Reinstallare solo se il file è mancante.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| o    | Reinstallare se il file è mancante o è una versione precedente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| h    | Reinstallare se il file è mancante o è una versione uguale o precedente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| d    | Reinstallare se il file è mancante o se è presente una versione diversa.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| c    | Verificare i valori di checksum e reinstallare il file se sono mancanti o danneggiati. Questo flag ripristina solo i file con msidbFileAttributesChecksum nella colonna attributi della [tabella file](file-table.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| a    | Consente di forzare la reinstallazione di tutti i file, indipendentemente dal checksum o dalla versione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| u    | Riscrivere tutte le voci del registro di sistema necessarie dalla [tabella del registro di sistema](registry-table.md) che passa all'**\_ \_ utente corrente di HKEY**<br/> o **HKEY \_ utenti**<br/> hive del registro di sistema.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| m    | Riscrivere tutte le voci del registro di sistema richieste dalla [tabella del registro di sistema](registry-table.md) che passano al **\_ \_ computer locale HKEY**<br/> o **HKEY \_ classi \_ radice**<br/> hive del registro di sistema. Riscrivere tutte le informazioni della tabella delle [classi](class-table.md), della tabella dei [verbi](verb-table.md), della tabella [PublishComponent](publishcomponent-table.md), della [tabella ProgId](progid-table.md), della tabella [MIME](mime-table.md), della [tabella delle icone](icon-table.md), della [tabella di estensione](extension-table.md)e della [tabella AppID](appid-table.md) indipendentemente dall'assegnazione del computer o dell'utente. Reinstallare tutti i [**componenti qualificati.**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) Quando si reinstalla un'applicazione, questa opzione esegue le azioni [RegisterTypeLibraries](registertypelibraries-action.md) e [InstallODBC](installodbc-action.md) .<br/> |
| s    | Reinstallare tutti i tasti di scelta rapida e rimemorizzare nella cache tutte le icone sovrascrivendo eventuali collegamenti e icone esistenti.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| v    | Utilizzare per eseguire dal pacchetto di origine e rimemorizzare nella cache il pacchetto locale. Non usare il codice dell'opzione di reinstallazione v per la prima installazione di un'applicazione o di una funzionalità.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

Se la proprietà **REINSTALLMODE** è definita senza definire anche la proprietà [**REINSTALL**](reinstall.md) , le modalità "rilevamento" specificate si applicano e specificano la modalità di "sovrascrittura" per un'installazione normale. La proprietà **REINSTALLMODE** influiscono solo sulle funzionalità selezionate normalmente per l'installazione. La presenza della proprietà **REINSTALLMODE** non reinstalla le funzionalità di. Per la reinstallazione delle funzionalità è richiesta la presenza della proprietà **REINSTALL** .

I codici di opzione per questa proprietà corrispondono all' [opzione della riga di comando](command-line-options.md) "/f". Il valore predefinito dell'opzione della riga di comando è' pecms '.

> [!Note]  
> Solo i file contenenti informazioni di checksum vengono sempre verificati e corretti. Il \_ flag FILEVERIFY REINSTALLMODE (CCODE precedente) Ripristina solo i file con msidbFileAttributesChecksum nella colonna attributi della [tabella file](file-table.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




