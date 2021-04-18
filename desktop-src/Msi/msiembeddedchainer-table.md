---
description: Usare questa tabella per creare un'installazione con più pacchetti.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Tabella MsiEmbeddedChainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902a33bce5d3a0aff3d2797fce94e5d272b61271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310521"
---
# <a name="msiembeddedchainer-table"></a>Tabella MsiEmbeddedChainer

Usare questa tabella per creare un' [installazione con più pacchetti](multiple-package-installations.md). Ogni riga della tabella MsiEmbeddedChainer fa riferimento a una funzione definita dall'utente diversa che può essere utilizzata per installare più pacchetti di Windows Installer da un singolo pacchetto. I [file eseguibili](executable-files.md) per le funzioni definite dall'utente vengono archiviati all'interno del pacchetto di Windows Installer.

**[Windows Installer 4,0 o versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. Questa tabella è disponibile a partire da Windows Installer 4,5.

**Windows Server 2008 R2 con il ruolo [Servizi Desktop remoto](../termserv/terminal-services-portal.md) abilitato:** Non supportato. L'installazione di più pacchetti con la tabella MsiEmbeddedChainer ha esito negativo se il ruolo [Servizi Desktop remoto](../termserv/terminal-services-portal.md) è abilitato.

Per installare più pacchetti da un singolo pacchetto, una delle funzioni definite dall'utente elencate nella tabella MsiEmbeddedChainer deve disporre di un'istruzione condizionale nel campo condizione che restituisce per eseguire l'azione. Se più di una funzione dispone di una condizione che restituisce l'esecuzione, è possibile eseguire una sola funzione. Questo caso è un errore e non è possibile garantire la funzione che verrà eseguita. Se per l'installazione sono necessarie altre azioni personalizzate, queste devono essere create nella [tabella CustomAction](customaction-table.md) e nelle tabelle di sequenza.

Le funzioni devono partecipare all'installazione corrente chiamando la funzione [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) e devono chiamare la funzione [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) per eseguire il commit dell'installazione di più pacchetti. Se le funzioni restituiscono prima di chiamare **MsiEndTransaction**, il programma di installazione esegue il rollback di tutte le installazioni.

La tabella MsiEmbeddedChainer include le colonne seguenti.



| Colonna             | Tipo                             | Chiave | Nullable |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [Identificatore](identifier.md)     | S   | N        |
| Condizione          | [Condition](condition.md)       | N   | S        |
| CommandLine        | [Formattato](formatted.md)       | N   | S        |
| Source (Sorgente)             | [CustomSource](customsource.md) | N   | N        |
| Tipo               | [Integer](integer.md)           | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer
</dt> <dd>

Chiave primaria per la tabella. Questo valore è un identificatore univoco per la funzione definita dall'utente descritta da questa riga.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condizione
</dt> <dd>

Istruzione condizionale per l'esecuzione della funzione definita dall'utente. È possibile abilitare o disabilitare le funzioni elencate nella tabella MsiEmbeddedChainer usando una trasformazione che modifica i valori delle proprietà valutati da questo campo. Per ulteriori informazioni, vedere [utilizzo delle proprietà nelle istruzioni condizionali](using-properties-in-conditional-statements.md).

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>CommandLine
</dt> <dd>

Il valore in questo campo fa parte della stringa della riga di comando passata al file eseguibile identificato nella colonna di origine. Il programma di installazione aggiunge il valore in questo campo all'handle di transazione per generare la riga di comando. Se il valore di questa colonna è null, la riga di comando è costituita solo dall'handle di transazione.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Origine
</dt> <dd>

Percorso del file eseguibile per la funzione definita dall'utente. Se il valore nella colonna Type è 2, questa colonna può contenere una chiave esterna nella [tabella binaria](binary-table.md). Se il valore nella colonna tipo è 18, questa colonna può contenere una chiave esterna nella [tabella file](file-table.md). Se il valore nella colonna tipo è 50, questa colonna può contenere una chiave esterna nella tabella delle [Proprietà](property-table.md).

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Le funzioni elencate nella tabella MsiEmbeddedChainer vengono descritte usando i tipi numerici dell'azione personalizzata seguenti. Questa colonna può contenere solo i valori per i seguenti tre tipi numerici. qualsiasi altra combinazione di flag di azione personalizzati viene ignorata.



| Tipo di azione personalizzata                                 | Flag azione personalizzati                                                | Valore esadecimale | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Tipo di azione personalizzata 2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [Tipo di azione personalizzata 18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [Tipo di azione personalizzata 50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il Windows Installer non impedisce l'esecuzione delle funzioni definite dall'utente in questa tabella durante l'annuncio dell'applicazione. È possibile utilizzare un'istruzione condizionale nella colonna Condition per impedire l'esecuzione di una funzione durante l'annuncio.

Il Windows Installer fornisce inoltre un gestore dell'interfaccia utente esterno non incorporato per creare un'interfaccia utente avanzata oltre al pacchetto di Windows Installer. Per ulteriori informazioni sull'utilizzo di un gestore dell'interfaccia utente esterno con la Windows Installer, vedere [monitoraggio di un'installazione mediante MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md).

La [tabella MsiPackageCertificate](msipackagecertificate-table.md) elenca i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che effettuano l'installazione di più pacchetti. È possibile utilizzare questa tabella per ridurre il numero di volte in cui l'installazione di più pacchetti Visualizza un messaggio di [*controllo dell'account utente*](u-gly.md) (UAC) che richiede una risposta da parte di un amministratore.

 

 
