---
description: La tabella MsiPatchSequence contiene tutte le informazioni richieste dal programma di installazione per determinare la sequenza di applicazione di una patch di aggiornamento ridotta rispetto a tutte le altre patch.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabella MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e63252b98156a5eac1ebdc5ed5d94c7a42ec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318657"
---
# <a name="msipatchsequence-table"></a>Tabella MsiPatchSequence

La tabella MsiPatchSequence contiene tutte le informazioni richieste dal programma di installazione per determinare la sequenza di applicazione di una patch di [aggiornamento ridotta](small-updates.md) rispetto a tutte le altre patch. La tabella deve trovarsi nel database del file di correzione e non in una trasformazione della patch. Quando si applica una patch di [aggiornamento principale](major-upgrades.md) , il programma di installazione ignora questa tabella. Quando si applica una patch di [aggiornamento secondaria](minor-upgrades.md) , il programma di installazione usa questa tabella solo per identificare le patch sostituite che non devono essere sequenziate.

La **tabella MsiPatchSequence** include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| PatchFamily | [Identificatore](identifier.md) | S   | N        |
| ProductCode | [GUID](guid.md)             | S   | S        |
| Sequenza    | [Versione](version.md)       | N   | N        |
| Attributi  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Specifica che la patch è un membro della famiglia di patch denominata in questo campo. Le patch presenti nella stessa famiglia di patch destinate alla stessa versione del prodotto vengono ordinate in base ai valori nella colonna sequenza. Le patch all'interno della famiglia di patch vengono applicate al prodotto di destinazione in ordine di sequenza crescente. PatchFamily viene utilizzato anche per determinare quali patch devono essere sostituite. È possibile che una patch venga elencata in più righe e appartenga a più famiglie di patch se si applica a più di un prodotto o include più correzioni.

Il Windows Installer non interpreta il valore PatchFamily in alcun modo diverso dai confronti per l'uguaglianza rispetto ad altri valori PatchFamily. Un valore PatchFamily deve essere univoco all'interno del ProductCode di destinazione dal set di patch. Negli scenari di applicazione di patch complessi l'identificatore PatchFamily può essere univoco a livello globale.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode
</dt> <dd>

Un valore in questo campo è facoltativo. Se in questo campo viene immesso un GUID del [Codice prodotto](product-codes.md) e la patch viene applicata al prodotto specificato, la patch viene ordinata e applicata come membro del PatchFamily specificato. Se in questo campo viene immesso un GUID del codice prodotto e la patch non viene applicata al prodotto specificato da ProductCode, la riga viene ignorata. Se il valore in ProductCode è NULL, la patch viene ordinata e applicata come membro di PatchFamily per tutte le destinazioni della patch, indipendentemente dal codice del prodotto.

Una patch può includere più righe nello stesso PatchFamily e un ProductCode diverso per ogni prodotto di destinazione della patch. Una riga per PatchFamily può specificare NULL per ProductCode. Se il prodotto di destinazione corrisponde a una riga con un valore di ProductCode non NULL, il programma di installazione utilizza la riga corrispondente e ignora la riga con il ProductCode NULL. Se nessuno dei codici prodotto specificati corrisponde alla destinazione, la patch viene ordinata e applicata come membro di PatchFamily per tutte le destinazioni della patch, indipendentemente dal codice del prodotto.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Il valore nella colonna sequenza specifica la sequenza di questa patch all'interno del PatchFamily specificato. Il valore in sequenza è espresso nel formato dati della [versione](version.md) . Il valore contiene tra 1 e 4 campi e ogni campo ha un intervallo compreso tra 0 e 65535. I membri di PatchFamily vengono ordinati e applicati al prodotto di destinazione in ordine di incremento dei valori di sequenza. Ad esempio, i sei valori seguenti sono in aumento: 1, 1,1, 1,2, 2,01, 2.01.1, 2.01.1.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

La presenza dell'attributo **msidbPatchSequenceSupersedeEarlier** in una riga indica che la patch di [aggiornamento di piccole dimensioni](small-updates.md) sostituisce gli aggiornamenti forniti da tutte le patch con valori di sequenza minori nello stesso PatchFamily. Questa patch contiene tutte le correzioni fornite dalle patch precedenti nel PatchFamily specificato. Questo attributo non significa che questa patch sostituisce le patch precedenti in tutti i casi, perché le patch precedenti possono appartenere a più famiglie di patch.

Una patch di [aggiornamento di dimensioni ridotte](small-updates.md) non può sostituire un [aggiornamento secondario](minor-upgrades.md) o una patch di [aggiornamento principale](major-upgrades.md) in qualsiasi circostanza, anche se **msidbPatchSequenceSupersedeEarlier** è impostato. 

| Nome                                   | Valore | Significato                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | Indica un semplice valore di sequenziazione.                              |
| **msidbPatchSequenceSupersedeEarlier** | 0x01  | Indica una patch che sostituisce le patch precedenti in questa famiglia. |



 

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



