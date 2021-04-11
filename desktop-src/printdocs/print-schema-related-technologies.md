---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 360325dc-51b5-44d5-981b-b69f7d6c82fd
title: Tecnologie Schema-Related di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8618493c2d24e8aebd7609c893d9de5a675bf24f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104132210"
---
# <a name="print-schema-related-technologies"></a>Tecnologie Schema-Related di stampa

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Per la .NET Framework 3,0, Windows Vista e versioni successive, le tecnologie PrintCapabilities e PrintTicket estendono le funzionalità dello schema di stampa per consentire un'esperienza di stampa più avanzata.

## <a name="printcapabilities"></a>PrintCapabilities

La tecnologia PrintCapabilities è un metodo per la pubblicazione della descrizione delle impostazioni controllabili dall'utente per gli attributi e le impostazioni per processo. PrintCapabilities sono pubblicate in un documento XML (eXtensible Markup Language) denominato documento PrintCapabilities, costituito da termini definiti nelle parole chiave dello schema di stampa e nelle estensioni private. Il documento PrintCapabilities può essere considerato come uno "snapshot" dello stato configurabile dall'utente per la configurazione del dispositivo corrente e una descrizione delle possibili configurazioni. I dispositivi (o i driver di dispositivo) generano un documento PrintCapabilities (snapshot) del set di opzioni configurabile corrente quando viene eseguita una query da parte dei client, che possono essere applicazioni o il sottosistema di stampa. Questo documento descrive tutti i PrintCapabilities configurabili attualmente disponibili nel dispositivo, ad esempio le opzioni di completamento e le opzioni di layout della pagina. Il documento PrintCapabilities descrive in modo esplicito tutti gli attributi del dispositivo e le impostazioni consentite per ogni attributo. Tramite l'utilizzo del Framework dello schema di stampa, gli attributi del dispositivo possono essere accuratamente descritti ed efficacemente confrontati. Utilizzando le parole chiave contenute nel documento delle parole chiave dello schema di stampa e la struttura definita in Print Schema Framework, i dispositivi possono consentire ai client di utilizzare in modo più efficace PrintCapabilities. Per ulteriori informazioni, vedere la pagina relativa alla [costruzione di schemi e documenti PrintCapabilities](printcapabilities-schema-and-document-construction.md).

Rispetto al sottosistema di stampa in Microsoft Windows Server 2003 e versioni precedenti, la tecnologia PrintCapabilities consente ai componenti del sottosistema client e di stampa di visualizzare in modo trasparente le informazioni contenute nell'elemento PrintCapabilities binario di sistema Win32 corrente. Ciò consente al client di eseguire query su PrintCapabilities, ricevere uno snapshot XML coerente e ben noto e utilizzarlo per costruire un oggetto PrintTicket per un dispositivo senza richiamare l'interfaccia utente del driver (UI).

## <a name="printticket"></a>PrintTicket

La tecnologia PrintTicket è il successore della struttura DEVMODE corrente. Si tratta di un documento basato sul linguaggio di markup estendibile che specifica e rende permanente le informazioni sulla formattazione dei processi e sulla configurazione del processo di stampa. Un'istanza PrintTicket assegna impostazioni specifiche del dispositivo e comunica la finalità dell'utente. Esistono due tipi di PrintTicket: gli PrintTicket generici, che non vengono generati per un particolare dispositivo; e PrintTicket specifici del dispositivo, costruiti per un determinato dispositivo. Gli PrintTicket generici, che devono essere portabili tra i dispositivi, derivano il contenuto selezionando le impostazioni per ognuno degli attributi del dispositivo descritti esclusivamente nelle parole chiave dello schema di stampa. Gli PrintTicket specifici del dispositivo derivano il loro contenuto da un documento PrintCapabilities, selezionando le impostazioni per ogni attributo del dispositivo annunciato dal documento. Questi PrintTicket possono includere anche estensioni private, specifiche di un modello di dispositivo o di un gruppo di modelli di dispositivo. Per ulteriori informazioni, vedere la pagina relativa alla [costruzione di schemi e documenti PrintTicket](printticket-schema-and-document-construction.md).

Rispetto al sottosistema di stampa corrente, la tecnologia PrintTicket consente a tutti i componenti e ai client del sottosistema di stampa di accedere in modo trasparente alle informazioni attualmente archiviate nelle parti Public e private della struttura DEVMODE, usando un formato XML ben definito. Questo progetto risolve i problemi correnti riscontrati negli scenari di aggiornamento del driver o di downgrade e di mancata corrispondenza dei driver nei driver progettati per la tecnologia PrintTicket. Questi scenari possono attualmente causare una perdita di impostazioni e quindi un'esperienza utente negativa. Il PrintTicket consente inoltre nuovi scenari, ad esempio l'abilitazione di un driver della stampante per esporre le impostazioni di DEVMODE privato ad applicazioni e plug-in personalizzati in modo coerente e non ambiguo. In questo modo, i componenti di stampa possono essere più trasparenti e gestire le migrazioni delle impostazioni in modo più semplice. Le interfacce PrintTicket verranno esposte alle applicazioni tramite metodi su oggetti di codice gestito che saranno disponibili anche per gli script. Nel nuovo Framework di applicazione basato sugli oggetti di codice gestito nella .NET Framework 3,0, l'oggetto PrintTicket rappresenta il modo standard per descrivere le impostazioni del documento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



