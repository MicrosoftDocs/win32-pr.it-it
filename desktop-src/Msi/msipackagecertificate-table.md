---
description: Nella tabella MsiPackageCertificate sono elencati i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che Multiple-Package installazione.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabella MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62abfa23f5e86949d6254ab89f7d70f01a8a4a8fe138a4eba114d2a45559390f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944519"
---
# <a name="msipackagecertificate-table"></a>Tabella MsiPackageCertificate

La tabella MsiPackageCertificate elenca i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che effettuano [l'installazione di più pacchetti.](multiple-package-installations.md)

Usare questa tabella per creare [un'installazione](multiple-package-installations.md) con più pacchetti per un prodotto contenente più Windows di installazione. Se il primo pacchetto è firmato digitalmente e contiene una tabella MsiPackageCertificate che specifica i certificati [](u-gly.md) digitali per tutti i pacchetti rimanenti nel prodotto, l'amministratore deve accettare solo la richiesta di controllo dell'account utente visualizzata per il primo pacchetto. Dopo aver accettato la richiesta del controllo dell'account utente per il primo pacchetto, le funzioni definite dall'utente nella tabella [MsiEmbeddedChainer](msiembeddedchainer-table.md) possono quindi unire i pacchetti rimanenti all'installazione di più pacchetti senza visualizzare una richiesta di controllo dell'account utente e richiedere una risposta dell'amministratore per ogni pacchetto.

Se una o più funzioni nella tabella [MsiEmbeddedChainer](msiembeddedchainer-table.md) richiedono un pacchetto non firmato, viene visualizzata un'altra richiesta di controllo dell'account utente che richiede l'interazione dell'amministratore per ogni pacchetto non firmato. Se l'amministratore accetta questa richiesta di controllo dell'account utente, l'installazione di più pacchetti continua. Dopo che un amministratore ha fornito le credenziali per un pacchetto, non verrà più visualizzata alcuna richiesta di controllo dell'account utente per il pacchetto durante l'installazione di più pacchetti. Se l'amministratore rifiuta una richiesta di controllo dell'account utente per un pacchetto, il programma di installazione di Windows esegue il rollback dell'installazione di più pacchetti prima di eseguire il commit dell'installazione di tutti i pacchetti appartenenti al prodotto.

**[Windows Installer 4.0 o versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato. Questa tabella è disponibile a partire da Windows Installer 4.5.

La tabella MsiPackageCertificate include le colonne seguenti:



| Colonna               | Tipo                         | Chiave | Nullable |
|----------------------|------------------------------|-----|----------|
| PackageCertificate   | [Identificatore](identifier.md) | S   | N        |
| DigitalCertificate\_ | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate
</dt> <dd>

Identificatore univoco per questa riga nella tabella MsiPackageCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Una chiave esterna nella prima colonna della tabella [MsiDigitalCertificate](msidigitalcertificate-table.md). La riga indicata nella tabella MsiDigitalCertificate contiene la rappresentazione binaria del certificato del firmatario.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE39](ice39.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MsiEmbeddedChainer](msiembeddedchainer-table.md)
</dt> <dt>

[Tabella MsiDigitalCertificate](msidigitalcertificate-table.md)
</dt> </dl>

 

 



