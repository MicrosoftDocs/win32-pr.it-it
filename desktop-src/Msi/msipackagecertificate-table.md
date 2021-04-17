---
description: La tabella MsiPackageCertificate elenca i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che rendono questo Multiple-Package installazione.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabella MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234036"
---
# <a name="msipackagecertificate-table"></a>Tabella MsiPackageCertificate

La tabella MsiPackageCertificate elenca i certificati di firma digitale usati per verificare l'identità dei pacchetti di installazione che rendono questa [installazione di più pacchetti](multiple-package-installations.md).

Usare questa tabella per creare un' [installazione di più pacchetti](multiple-package-installations.md) per un prodotto contenente più pacchetti Windows Installer. Se il primo pacchetto è firmato digitalmente e contiene una tabella MsiPackageCertificate che specifica i certificati digitali per tutti i pacchetti rimanenti del prodotto, l'amministratore deve accettare solo la richiesta di [*controllo dell'account utente*](u-gly.md) (UAC) visualizzata per il primo pacchetto. Dopo aver accettato la richiesta del controllo dell'account utente per il primo pacchetto, le funzioni definite dall'utente nella [tabella MsiEmbeddedChainer](msiembeddedchainer-table.md) possono quindi aggiungere i pacchetti rimanenti all'installazione di più pacchetti senza visualizzare una richiesta di controllo dell'account utente e richiedere una risposta dell'amministratore per ogni pacchetto.

Se una o più funzioni nella [tabella MsiEmbeddedChainer](msiembeddedchainer-table.md) richiedono un pacchetto non firmato, viene visualizzato un altro messaggio di controllo dell'account utente che richiede l'interazione dell'amministratore per ogni pacchetto non firmato. Se l'amministratore accetta questa richiesta di controllo dell'account utente, l'installazione di più pacchetti continua. Una volta che un amministratore ha fornito le credenziali per un pacchetto, durante l'installazione di più pacchetti non verrà visualizzato alcun messaggio di richiesta del controllo dell'account utente per tale pacchetto. Se l'amministratore rifiuta una richiesta di controllo dell'account utente per un pacchetto, Windows Installer esegue il rollback dell'installazione di più pacchetti prima di eseguire il commit per installare i pacchetti appartenenti al prodotto.

**[Windows Installer 4,0 o versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. Questa tabella è disponibile a partire da Windows Installer 4,5.

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

Chiave esterna nella prima colonna della [tabella MsiDigitalCertificate](msidigitalcertificate-table.md). La riga indicata nella tabella MsiDigitalCertificate contiene la rappresentazione binaria del certificato del firmatario.

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

 

 



