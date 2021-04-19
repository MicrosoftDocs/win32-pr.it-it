---
description: La proprietà FASTOEM è progettata per consentire agli OEM di ridurre il tempo necessario per l'installazione di applicazioni Windows Installer per uno scenario specifico.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: Proprietà FASTOEM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332956"
---
# <a name="fastoem-property"></a>Proprietà FASTOEM

La proprietà **FASTOEM** è progettata per consentire agli OEM di ridurre il tempo necessario per l'installazione di applicazioni Windows Installer per uno scenario specifico. Non creare la proprietà **FASTOEM** nella tabella delle [Proprietà](property-table.md).

La proprietà **FASTOEM** è applicabile solo se si verificano tutte le condizioni seguenti:

-   L'applicazione viene installata nello stesso volume della cartella che contiene i file di origine.
-   I file di origine vengono eliminati dopo l'installazione.
-   Durante l'installazione non viene visualizzata alcuna interfaccia utente. Il [livello dell'interfaccia utente](user-interface-levels.md) è None.
-   L'installazione viene eseguita nel [contesto di installazione](installation-context.md)per computer.
-   Lo spazio disponibile nel computer è sufficiente per una corretta installazione.
-   Questa è la prima volta che si installa. L'installazione non sta annunciando, reinstallando, rimuovendo o eseguendo un'installazione amministrativa.
-   Nessuna funzionalità installata per l'esecuzione dall'origine.
-   Il pacchetto di installazione non contiene [componenti isolati](isolated-components.md). Poiché i componenti isolati richiedono che i file di origine rimangano nell'origine, non è attualmente possibile utilizzare la proprietà **FASTOEM** con componenti isolati.

Se tutte le condizioni precedenti sono vere, l'impostazione della proprietà **FASTOEM** consente Windows Installer per migliorare le prestazioni effettuando le operazioni seguenti:

-   Spostare invece di copiare i file nello stesso volume. Ciò non garantisce che tutti i file vengano spostati anziché copiati. Si noti che se il computer dispone di più dischi rigidi, è necessario inizializzare la proprietà [**ROOTDRIVE**](rootdrive.md) nella riga di comando nella stessa unità contenente l'origine dell'installazione.
-   Omettere questa origine dall'elenco di origine dell'applicazione in modo che le installazioni successive di reinstallazione o manutenzione siano predefinite per le origini CD-ROM specificate nella [tabella media](media-table.md).
-   Semplifica il [costo del file](file-costing.md).
-   Non visualizzare i messaggi di stato inviati dal Windows Installer al client.

## <a name="remarks"></a>Commenti

Poiché non vengono inviati messaggi di stato quando viene impostato **FASTOEM** , è consigliabile che gli autori scrivano manualmente un valore di 1800 per il timeout nella chiave

**HKLM** \\ **Software** \\ di **Criteri** \\ di **Microsoft** \\ **Windows** \\ **Programma di installazione** \\ **Timeout**

Timeout è un tipo **reg \_ DWORD** .

Per visualizzare le dimensioni dell'applicazione in Installazione applicazioni nel pannello di controllo di Windows 2000, è necessario scrivere manualmente il valore di EstimatedSize nella chiave

**HKLM** \\ **Software** \\ di **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Disinstalla** \\ **<  Codice > prodotto**

Si tratta di un tipo **reg \_ DWORD** ed è uguale alla dimensione dell'applicazione in Kbyte. Il programma di installazione non scrive automaticamente questo valore.

Usare la riga di comando di esempio seguente se il CD-ROM spedito agli utenti finali archivia il pacchetto di installazione dell'applicazione nella directory principale del CD-ROM. Si noti che l'etichetta del volume nella [tabella media](media-table.md) del file con estensione msi deve corrispondere all'etichetta del volume del CD-ROM.

**Msiexec/I C: \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 DisableRollback = 1 ROOTDRIVE = C:\\**

Usare la riga di comando di esempio seguente se il pacchetto di installazione non si trova nella directory principale del CD-ROM spedito agli utenti finali. È necessario impostare la proprietà [**MEDIAPACKAGEPATH**](mediapackagepath.md) in questo caso sul percorso del pacchetto di installazione. L'etichetta del volume nella [tabella media](media-table.md) del file con estensione msi deve corrispondere all'etichetta del volume del CD-ROM. In questo caso, seguire questo esempio.

**Msiexec/I C: \\ TempImage \\package.msi/qn/le logfile.txt ALLUSERS = 1 FASTOEM = 1 DisableRollback = 1 MEDIAPACKAGEPATH = c: \\ TempImage \\package.msi ROOTDRIVE = c:\\**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




