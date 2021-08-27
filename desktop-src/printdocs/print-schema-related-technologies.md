---
description: Esplorare le tecnologie correlate allo schema di stampa. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: Tecnologie di Schema-Related stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2948108b8bd6f581608471c9646fe135f83cb91561dc3c4cca97ac4df10560
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112271"
---
# <a name="print-schema-related-technologies"></a>Tecnologie di Schema-Related stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Per .NET Framework 3.0, Windows Vista e versioni successive, le tecnologie PrintCapabilities e PrintTicket estendono le funzionalità dello schema di stampa per consentire un'esperienza di stampa più dettagliata.

## <a name="printcapabilities"></a>PrintCapabilities

La tecnologia PrintCapabilities è un metodo per pubblicare la descrizione delle impostazioni controllabili dall'utente degli attributi e delle impostazioni per processo. PrintCapabilities viene pubblicato in un documento XML (eXtensible Markup Language) denominato documento PrintCapabilities, costituito da termini definiti nelle parole chiave dello schema di stampa e nelle estensioni private. Il documento PrintCapabilities può essere pensato come uno "snapshot" della configurazione corrente del dispositivo dello stato configurabile dall'utente, nonché una descrizione delle possibili configurazioni. I dispositivi (o driver di dispositivo) generano un documento PrintCapabilities (lo snapshot) del set corrente di opzioni configurabili quando vengono sottoposti a query dai client, che possono essere applicazioni o il sottosistema di stampa. Questo documento descrive tutte le printcapabilities configurabili attualmente disponibili nel dispositivo, ad esempio le opzioni di completamento e le opzioni di layout di pagina. Il documento PrintCapabilities descrive in modo esplicito tutti gli attributi del dispositivo e le impostazioni consentite per ogni attributo. Tramite l'uso di Print Schema Framework, gli attributi del dispositivo possono essere descritti con precisione ed essere confrontati in modo efficiente. Usando le parole chiave contenute nel documento Print Schema Keywords e la struttura definita in Print Schema Framework, i dispositivi possono consentire ai client di usare in modo più efficace PrintCapabilities. Per altre informazioni, vedere [Schema PrintCapabilities e Costruzione di documenti.](printcapabilities-schema-and-document-construction.md)

Rispetto al sottosistema di stampa in Microsoft Windows Server 2003 e versioni precedenti, la tecnologia PrintCapabilities consente ai componenti del client e del sottosistema di stampa di visualizzare in modo trasparente le informazioni contenute nel file binario di sistema Win32 corrente PrintCapabilities. In questo modo il client può eseguire query su PrintCapabilities, ricevere uno snapshot XML coerente e ben compreso e usarlo per costruire un PrintTicket per un dispositivo senza richiamare l'interfaccia utente del driver.

## <a name="printticket"></a>PrintTicket

La tecnologia PrintTicket è il successore della struttura DEVMODE corrente. Si tratta di un documento basato su eXtensible Markup Language che specifica e rende persistenti le informazioni sulla formattazione del processo e sulla configurazione del processo di stampa. Un'istanza di PrintTicket assegna impostazioni specifiche del dispositivo e indica la finalità dell'utente. Esistono due tipi di PrintTicket: PrintTicket generici, che non vengono generati per un particolare dispositivo; e printTicket specifici del dispositivo, costruiti per un particolare dispositivo. Gli oggetti PrintTicket generici, che devono essere portabili tra dispositivi, derivano il contenuto selezionando le impostazioni per ognuno degli attributi del dispositivo descritti esclusivamente nelle parole chiave dello schema di stampa. I PrintTicket specifici del dispositivo derivano il contenuto da un documento PrintCapabilities, selezionando le impostazioni per ogni attributo del dispositivo annunciato da questo documento. Questi PrintTicket possono includere anche estensioni private, specifiche di un modello di dispositivo o di una famiglia di modelli di dispositivo. Per altre informazioni, vedere [Schema PrintTicket e Costruzione di documenti.](printticket-schema-and-document-construction.md)

Rispetto al sottosistema di stampa corrente, la tecnologia PrintTicket consente a tutti i componenti e client del sottosistema di stampa di accedere in modo trasparente alle informazioni attualmente archiviate nelle parti pubbliche e private della struttura DEVMODE, usando un formato XML ben definito. Questa progettazione risolve i problemi correnti riscontrati negli scenari di aggiornamento o downgrade e mancata corrispondenza dei driver nei driver progettati per la tecnologia PrintTicket. Questi scenari possono attualmente comportare la perdita di impostazioni e quindi un'esperienza negativa per i clienti. PrintTicket consente anche nuovi scenari, ad esempio l'abilitazione di un driver della stampante per esporre le impostazioni DEVMODE private alle applicazioni e ai plug-in personalizzati in modo coerente e non ambiguo. In questo modo i componenti di stampa sono più trasparenti e le migrazioni delle impostazioni vengono gestite in modo più pulito. Le interfacce PrintTicket verranno esposte alle applicazioni tramite metodi su oggetti di codice gestito che saranno disponibili anche per gli script. Nel nuovo framework applicazione basato su oggetti di codice gestito in .NET Framework 3.0, PrintTicket è il modo standard per descrivere le impostazioni dei documenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



