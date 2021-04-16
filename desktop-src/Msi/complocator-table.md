---
description: La tabella CompLocator contiene le informazioni necessarie per trovare un file o una directory che usa i dati di configurazione del programma di installazione.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Tabella CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530240"
---
# <a name="complocator-table"></a>Tabella CompLocator

La tabella CompLocator contiene le informazioni necessarie per trovare un file o una directory che usa i dati di configurazione del programma di installazione.

La tabella CompLocator contiene le informazioni seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificatore](identifier.md) | S   | N        |
| ComponentId | [GUID](guid.md)             | N   | N        |
| Tipo        | [Integer](integer.md)       | N   | S        |



 

## <a name="column-information"></a>Informazioni sulle colonne

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

Questa colonna rappresenta una firma del file univoca ed è anche la chiave esterna nella [tabella della firma](signature-table.md). Se la chiave è assente dalla tabella di firma, si presuppone che la ricerca sia per la presenza di una directory a cui punta la tabella CompLocator.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

ID del componente il cui percorso della chiave deve essere utilizzato per la ricerca. Deve corrispondere al GUID di un componente visualizzato nel campo ComponentId della [tabella Component](component-table.md). Potrebbe trattarsi dell'ID componente di un componente che appartiene a un altro prodotto installato nel computer. Non deve essere il GUID di un componente Pubblicato visualizzato nel campo ComponentId della [tabella PublishComponent](publishcomponent-table.md).

Per trovare il valore GUID ID componente per un file installato da un altro prodotto, passare al pacchetto di installazione del prodotto. Passare alla [tabella file](file-table.md) e individuare la riga che contiene l'identificatore del file. La \_ colonna Component di questa riga contiene l'identificatore del componente per il componente che controlla il file. Passare alla [tabella dei componenti](component-table.md) e trovare la riga che contiene l'identificatore del componente nella colonna componente. La colonna ComponentId di questa riga contiene il GUID ID componente.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Valore booleano che determina se il percorso della chiave del componente è un nome file o un percorso di directory.

Nella tabella seguente sono elencati i valori validi. Se assente, Type è impostato su 1 (uno).



| Costante                      | Valore esadecimale | Decimal | Descrizione              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Il percorso della chiave è una directory. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Il percorso della chiave è un nome di file. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene utilizzata con la [tabella AppSearch](appsearch-table.md).

In genere, le colonne in questa tabella non sono localizzate. Se un autore decide di cercare i prodotti in più lingue, è possibile che nella tabella sia inclusa una voce separata per ogni lingua.

Per ulteriori informazioni, vedere [ricerca di applicazioni esistenti, file, voci del registro di sistema o voci del file ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



