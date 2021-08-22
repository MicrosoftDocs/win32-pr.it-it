---
description: Usare questa tabella per creare un'installazione con più pacchetti.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Tabella MsiEmbeddedChainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfcf48f3cf3863f19819b3337a136d2540fa3254067cacc50fcf391256caa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945056"
---
# <a name="msiembeddedchainer-table"></a>Tabella MsiEmbeddedChainer

Usare questa tabella per creare [un'installazione con più pacchetti.](multiple-package-installations.md) Ogni riga nella tabella MsiEmbeddedChainer fa riferimento a una funzione definita dall'utente diversa che può essere usata per installare più pacchetti Windows Installer da un singolo pacchetto. I [file eseguibili](executable-files.md) per le funzioni definite dall'utente vengono archiviati all'interno del Windows Installer.

**[Windows Installer 4.0 o versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato. Questa tabella è disponibile a partire da Windows Installer 4.5.

**Windows Server 2008 R2 con il [ruolo Servizi Desktop remoto](../termserv/terminal-services-portal.md) abilitato:** Non supportato. L'installazione di più pacchetti tramite la tabella MsiEmbeddedChainer ha esito negativo [se il Servizi Desktop remoto](../termserv/terminal-services-portal.md) è abilitato.

Per installare più pacchetti da un singolo pacchetto, una delle funzioni definite dall'utente elencate nella tabella MsiEmbeddedChainer deve avere un'istruzione condizionale nel campo Condizione che restituirà l'esecuzione dell'azione. Se più funzioni hanno una condizione che restituisce l'esecuzione, è possibile eseguire una sola funzione. Questo caso è un errore e non è possibile garantire quale funzione verrà eseguita. Se altre azioni personalizzate sono necessarie per l'installazione, devono essere scritte nella tabella [CustomAction](customaction-table.md) e nelle tabelle di sequenza.

Le funzioni devono essere unite all'installazione corrente chiamando la funzione [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) e devono chiamare la [**funzione MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) per eseguire il commit dell'installazione di più pacchetti. Se le funzioni restituiscono prima di **chiamare MsiEndTransaction,** il programma di installazione esegue il rollback di tutte le installazioni.

La tabella MsiEmbeddedChainer contiene le colonne seguenti.



| Colonna             | Tipo                             | Chiave | Nullable |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [Identificatore](identifier.md)     | S   | N        |
| Condition          | [Condition](condition.md)       | N   | S        |
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

Istruzione condizionale per l'esecuzione della funzione definita dall'utente. È possibile abilitare o disabilitare le funzioni elencate nella tabella MsiEmbeddedChainer usando una trasformazione che modifica i valori delle proprietà valutati da questo campo. Per altre informazioni, vedere [Uso delle proprietà nelle istruzioni condizionali.](using-properties-in-conditional-statements.md)

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>Commandline
</dt> <dd>

Il valore in questo campo fa parte della stringa della riga di comando passata al file eseguibile identificato nella colonna Source. Il programma di installazione aggiunge il valore in questo campo all'handle della transazione per generare la riga di comando. Se il valore in questa colonna è Null, la riga di comando è costituita solo dall'handle della transazione.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>fonte
</dt> <dd>

Percorso del file eseguibile per la funzione definita dall'utente. Se il valore nella colonna Tipo è 2, questa colonna può contenere una chiave esterna nella [tabella binaria](binary-table.md). Se il valore nella colonna Tipo è 18, questa colonna può contenere una chiave esterna nella [tabella File](file-table.md). Se il valore nella colonna Type è 50, questa colonna può contenere una chiave esterna nella [tabella Property](property-table.md).

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>digitare
</dt> <dd>

Le funzioni elencate nella tabella MsiEmbeddedChainer vengono descritte usando i tipi numerici di azione personalizzata seguenti. Questa colonna può contenere i valori solo per i tre tipi numerici seguenti. Qualsiasi altra combinazione di flag di azione personalizzata viene ignorata.



| Tipo di azione personalizzata                                 | Flag di azione personalizzata                                                | Valore esadecimale | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Tipo di azione personalizzata 2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [Tipo di azione personalizzata 18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [Tipo di azione personalizzata 50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il Windows non impedisce l'esecuzione delle funzioni definite dall'utente in questa tabella durante l'annuncio dell'applicazione. È possibile usare un'istruzione condizionale nella colonna Condizione per impedire l'esecuzione di una funzione durante l'annuncio.

Il Windows installer fornisce anche un gestore dell'interfaccia utente esterno non incorporato per compilare un'interfaccia utente rtf sopra il pacchetto Windows Installer. Per altre informazioni sull'uso di un gestore dell'interfaccia utente esterno con Windows, vedere Monitoring an Installation Using MsiSetExternalUI (Monitoraggio di un'installazione [tramite MsiSetExternalUI).](monitoring-an-installation-using-msisetexternalui.md)

La [tabella MsiPackageCertificate elenca](msipackagecertificate-table.md) i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che effettuano un'installazione con più pacchetti. È possibile usare questa tabella per ridurre il numero di volte in cui l'installazione di più pacchetti visualizza una richiesta di controllo dell'account utente [*che*](u-gly.md) richiede una risposta da parte di un amministratore.

 

 
