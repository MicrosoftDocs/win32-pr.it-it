---
description: La tabella MsiPatchSequence contiene tutte le informazioni richieste dal programma di installazione per determinare la sequenza di applicazione di una patch di aggiornamento di piccole dimensioni rispetto a tutte le altre patch.
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: Tabella MsiPatchSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc529c0f7d1a4cdd1bab568f64507922d6e28f539636600f88dea603c4fe1a52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519801"
---
# <a name="msipatchsequence-table"></a>Tabella MsiPatchSequence

La tabella MsiPatchSequence contiene tutte le informazioni necessarie al programma di installazione per determinare la sequenza di applicazione di una [patch](small-updates.md) di aggiornamento di piccole dimensioni rispetto a tutte le altre patch. La tabella deve essere nel database del file di patch e non in una trasformazione nella patch. Il programma di installazione ignora questa tabella quando si applica una patch [di aggiornamento principale.](major-upgrades.md) Quando si applica una patch [di aggiornamento](minor-upgrades.md) secondaria, il programma di installazione usa questa tabella solo per identificare le patch sostituite che non devono essere sequenziate.

La **tabella MsiPatchSequence** include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| PatchFamily | [Identificatore](identifier.md) | S   | N        |
| ProductCode | [GUID](guid.md)             | S   | S        |
| Sequenza    | [Version](version.md)       | N   | N        |
| Attributi  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

Specifica che la patch è un membro della famiglia di patch denominata in questo campo. Le patch nella stessa famiglia di patch che hanno come destinazione la stessa versione del prodotto vengono ordinate in base ai valori nella colonna Sequenza. Le patch all'interno della famiglia di patch vengono applicate al prodotto di destinazione nell'ordine di sequenza crescente. PatchFamily viene usato anche per determinare quali patch devono essere sostituite. Una patch può essere elencata in più righe e appartenere a più famiglie di patch se si applica a più prodotti o include più correzioni.

Il Windows Installer non interpreta il valore PatchFamily in alcun modo diverso dai confronti per verificarne l'uguaglianza con altri valori PatchFamily. Un valore PatchFamily deve essere univoco all'interno di ProductCode come destinazione del set di patch. Negli scenari di applicazione di patch complessi potrebbe essere necessario che l'identificatore PatchFamily sia univoco a livello globale.

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>Productcode
</dt> <dd>

Un valore in questo campo è facoltativo. Se [in](product-codes.md) questo campo viene immesso un GUID del codice prodotto e la patch viene applicata al prodotto specificato, la patch viene ordinata e applicata come membro dell'oggetto PatchFamily specificato. Se in questo campo viene immesso un GUID del codice prodotto e la patch non viene applicata al prodotto specificato da ProductCode, questa riga viene ignorata. Se il valore in ProductCode è NULL, la patch viene ordinata e applicata come membro di PatchFamily per tutte le destinazioni della patch indipendentemente dal codice del prodotto.

Una patch può avere più righe nella stessa PatchFamily e un Codice Product diverso per ogni prodotto di destinazione della patch. Una riga per PatchFamily può specificare NULL per ProductCode. Se il prodotto di destinazione corrisponde a una riga con un ProductCode diverso da NULL, il programma di installazione usa la riga corrispondente e ignora la riga con il codice ProductCode NULL. Se nessuno dei codici prodotto specificati corrisponde alla destinazione, la patch viene ordinata e applicata come membro di PatchFamily per tutte le destinazioni della patch indipendentemente dal codice del prodotto.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Il valore nella colonna Sequence specifica la sequenza di questa patch all'interno dell'oggetto PatchFamily specificato. Il valore in Sequence è espresso nel formato dei [dati version.](version.md) Il valore contiene da 1 a 4 campi e ogni campo ha un intervallo compreso tra 0 e 65535. I membri di PatchFamily vengono ordinati e applicati al prodotto di destinazione nell'ordine di valori Sequence crescenti. Ad esempio, i sei valori seguenti aumentano: 1, 1.1, 1.2, 2.01, 2.01.1, 2.01.1.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

La presenza dell'attributo **msidbPatchSequenceSupersedeEarlier** in una riga indica che la [patch](small-updates.md) di aggiornamento di piccole dimensioni sostituisce gli aggiornamenti forniti da tutte le patch con valori Sequence inferiori nella stessa patchFamily. Questa patch contiene tutte le correzioni fornite dalle patch precedenti nell'oggetto PatchFamily specificato. Questo attributo non significa che questa patch sostituisce le patch precedenti in tutti i casi, perché le patch precedenti possono appartenere a più famiglie di patch.

Una patch [di](small-updates.md) aggiornamento di [](minor-upgrades.md) piccole dimensioni non può sostituisce un aggiornamento secondario o una [patch](major-upgrades.md) di aggiornamento principale in qualsiasi circostanza, anche se è impostato **msidbPatchSequenceSupersedeEarlier.** 

| Nome                                   | Valore | Significato                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | Indica un valore di sequenziazione semplice.                              |
| **msidbPatchSequenceSupersedeEarlier** | 0x01  | Indica una patch che sostituisce le patch precedenti in questa famiglia. |



 

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



