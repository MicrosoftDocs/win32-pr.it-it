---
description: La tabella CompLocator contiene le informazioni necessarie per trovare un file o una directory che usa i dati di configurazione del programma di installazione.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Tabella CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6a51ad618521ff49b2a5b13f76fcfbae4207b5cdf4d77e76d3e128816bbb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145080"
---
# <a name="complocator-table"></a>Tabella CompLocator

La tabella CompLocator contiene le informazioni necessarie per trovare un file o una directory che usa i dati di configurazione del programma di installazione.

La tabella CompLocator contiene le informazioni seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Firma\_ | [Identificatore](identifier.md) | S   | N        |
| Componentid | [GUID](guid.md)             | N   | N        |
| Tipo        | [Integer](integer.md)       | N   | S        |



 

## <a name="column-information"></a>Informazioni sulle colonne

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_
</dt> <dd>

Questa colonna rappresenta una firma di file univoca ed è anche la chiave esterna nella [tabella della firma](signature-table.md). Se la chiave è assente dalla tabella delle firme, si presuppone che la ricerca sia per la presenza di una directory a cui punta la tabella CompLocator.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

ID componente del componente il cui percorso della chiave deve essere usato per la ricerca. Deve essere il GUID di un componente visualizzato nel campo ComponentId della [tabella dei componenti](component-table.md). Può trattarsi dell'ID componente di un componente appartenente a un altro prodotto installato nel computer. Non deve essere il GUID di un componente pubblicato visualizzato nel campo ComponentId della [tabella PublishComponent](publishcomponent-table.md).

Per trovare il valore GUID dell'ID componente per un file installato da un altro prodotto, passare al pacchetto di installazione del prodotto. Passare alla tabella [File e](file-table.md) trovare la riga che contiene l'identificatore di file per il file. La colonna \_ Componente di questa riga contiene l'identificatore del componente che controlla il file. Passare alla tabella [Componente e](component-table.md) trovare la riga che contiene l'identificatore del componente nella colonna Componente. La colonna ComponentId di questa riga contiene il GUID dell'ID componente.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>digitare
</dt> <dd>

Valore booleano che determina se il percorso della chiave del componente è un nome file o un percorso di directory.

Nella tabella seguente sono elencati i valori validi. Se assente, Type è impostato su 1 (uno).



| Costante                      | Valore esadecimale | Decimal | Descrizione              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Il percorso della chiave è una directory. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Il percorso della chiave è un nome di file. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene usata con [la tabella AppSearch](appsearch-table.md).

In genere, le colonne in questa tabella non sono localizzate. Se un autore decide di cercare prodotti in più lingue, nella tabella può essere inclusa una voce separata per ogni lingua.

Per altre informazioni, vedere [Ricerca di applicazioni, file, voci](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)del Registro di sistema o .ini file esistenti .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



