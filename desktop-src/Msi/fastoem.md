---
description: La proprietà FASTOEM è progettata per consentire agli OEM di ridurre il tempo necessario per installare Windows programma di installazione per uno scenario specifico.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: FASTOEM - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c882ee78645a7f3a0fd8cd2677ca7ddfabade9b4395202cbbf0ab547b12a19eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129581"
---
# <a name="fastoem-property"></a>FASTOEM - proprietà

La **proprietà FASTOEM** è progettata per consentire agli OEM di ridurre il tempo necessario per installare Windows programma di installazione per uno scenario specifico. Non creare la **proprietà FASTOEM** nella tabella [delle proprietà](property-table.md).

La **proprietà FASTOEM** è applicabile solo se tutte queste condizioni sono vere:

-   L'applicazione viene installata nello stesso volume della cartella contenente i file di origine.
-   I file di origine vengono eliminati dopo l'installazione.
-   Durante l'installazione non viene visualizzata alcuna interfaccia utente. Il [livello dell'interfaccia](user-interface-levels.md) utente non è nessuno.
-   L'installazione viene eseguita nel contesto di installazione per [computer.](installation-context.md)
-   Lo spazio disponibile nel computer è sufficiente per una corretta installazione.
-   Questa è la prima installazione. L'installazione non è in corso di annuncio, reinstallazione, rimozione o esecuzione di un'installazione amministrativa.
-   Non sono installate funzionalità per l'esecuzione dall'origine.
-   Il pacchetto di installazione non contiene [componenti isolati.](isolated-components.md) Poiché i componenti isolati richiedono che i file di origine rimangano all'origine, la **proprietà FASTOEM** non può attualmente essere usata con i componenti isolati.

Se tutte le condizioni precedenti sono vere, l'impostazione della proprietà **FASTOEM** consente Windows Installer di migliorare le prestazioni eseguendo le operazioni seguenti:

-   Spostare anziché copiare i file nello stesso volume. Ciò non garantisce che tutti i file siano spostati anziché copiati. Si noti che se il computer ha più dischi rigidi, è necessario inizializzare la proprietà [**ROOTDRIVE**](rootdrive.md) nella riga di comando sulla stessa unità contenente l'origine dell'installazione.
-   Omettere questa origine dall'elenco di origine dell'applicazione in modo che le successive installazioni di reinstallazione o manutenzione per impostazione predefinita si abilitino alle origini CD-ROM specificate nella [tabella dei supporti](media-table.md).
-   Semplificare [la determinazione dei costi dei file.](file-costing.md)
-   Eliminare i messaggi di stato inviati Windows programma di installazione al client.

## <a name="remarks"></a>Commenti

Poiché non vengono inviati messaggi di stato quando è impostato **FASTOEM,** è consigliabile che gli autori scrivono manualmente il valore 1800 per Timeout nella chiave

**HKLM** \\ **Software software** \\ **Criteri** \\ **Microsoft** \\ **Windows** \\ **Programma di installazione** \\ **Timeout**

Timeout è un **tipo \_ DWORD REG.**

Per visualizzare le dimensioni dell'applicazione in Installazione applicazioni nel Windows 2000 Pannello di controllo, è necessario scrivere manualmente il valore di EstimatedSize nella chiave

**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstallare** \\ **< *Codice prodotto* >**

Si tratta di **un \_ tipo REG DWORD** ed è uguale alla dimensione dell'applicazione in Kbyte. Il programma di installazione non scrive automaticamente questo valore.

Usare la riga di comando di esempio seguente se il CD-ROM fornito agli utenti finali archivia il pacchetto di installazione dell'applicazione nella radice del CD-ROM. Si noti che l'etichetta di volume nella tabella dei supporti del file .msi deve corrispondere all'etichetta di volume del CD-ROM. [](media-table.md)

**Msiexec /I C: \\ TempImage \\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**

Usare la riga di comando di esempio seguente se il pacchetto di installazione non si trova nella radice del CD-ROM fornito agli utenti finali. In questo caso è necessario impostare la proprietà [**MEDIAPACKAGEPATH**](mediapackagepath.md) sul percorso del pacchetto di installazione. L'etichetta di volume [nella tabella supporti](media-table.md) del file .msi deve corrispondere all'etichetta di volume del CD-ROM. In questo caso seguire questo esempio.

**Msiexec /I C: \\ TempImage \\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C: \\ TempImage \\package.msi ROOTDRIVE=C:\\**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Per informazioni [Windows service](windows-installer-portal.md) pack minimo necessario per Run-Time versione del programma di installazione di Windows, vedere i requisiti minimi Windows Service Pack.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




