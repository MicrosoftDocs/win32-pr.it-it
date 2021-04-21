---
title: Cronologia delle versioni di DirectML
description: DirectML viene distribuito come componente di sistema di Windows 10 ed è disponibile come parte del sistema operativo Windows 10 in Windows 10 versione 1903 (10.0; Build 18362) e versione più recente.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: f5e0a478b2d4c6728a1cd53388ba09af8e5bbc0e
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803943"
---
# <a name="directml-version-history"></a>Cronologia delle versioni di DirectML

DirectML viene distribuito come componente di sistema di Windows 10 ed è disponibile come parte del sistema operativo Windows 10 in Windows 10 versione 1903 (10.0; Build 18362) e versione più recente.

A partire da DirectML versione 1.4.0, DirectML è disponibile anche come pacchetto ridistribuibile autonomo (vedere [Microsoft.AI.DirectML),](https://www.nuget.org/packages/Microsoft.AI.DirectML/)utile per le applicazioni che vogliono usare una versione fissa di DirectML o quando vengono eseguite in versioni precedenti di Windows 10.

DirectML segue le [convenzioni di controllo delle versioni semantiche.](https://semver.org/) In altri, i numeri di versione seguono il formato `major.minor.patch` . La prima versione di DirectML ha una versione 1.0.0.

## <a name="version-table"></a>Tabella delle versioni

|Versione di DirectML|Livello di funzionalità supportato (vedere [Cronologia a livello di funzionalità DirectML](./dml-feature-level-history.md))|DML_TARGET_VERSION|Primo disponibile in|Primo disponibile in (Ridistribuibile)|
|-|-|-|-|-|-|
|1.5.0|DML_FEATURE_LEVEL_3_1|`0x3100`|N/D|[DirectML-1.5.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.5.0)|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|N/D|[DirectML-1.4.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/1.4.0)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10 versione 2004 (10.0; Build 19041) (aggiornamento Windows 10 maggio 2020). Noto anche come "20H1".|N/D|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10 versione 1903 (10.0; Build 18362) (Aggiornamento di Windows 10 (maggio 2019)). Noto anche come "19H1".|N/D|

<sup>1</sup> Le versioni intermedie 1.2.0 e 1.3.0 di DirectML non sono state rese ampiamente disponibili.

## <a name="selecting-a-directml-target-version"></a>Selezione di una versione di destinazione DirectML

Per praticità, alcune funzionalità nel `DirectML.h` file di intestazione vengono dichiarate in modo condizionale in base al valore della `DML_TARGET_VERSION` macro. Impostando la `DML_TARGET_VERSION` macro su determinati valori, è possibile escludere parti di `DirectML.h` dall'applicazione.

Ciò può essere utile se si usa una copia più recente di , ma la destinazione è una versione precedente del file binario DirectML, perché garantisce che qualsiasi tentativo di usare funzionalità oltre il livello di destinazione scelto non venga `DirectML.h` compilato. Questo meccanismo è simile alla `NTDDI_VERSION` macro (vedere [Macro per le dichiarazioni condizionali).](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)

Ecco i valori validi per la `DML_TARGET_VERSION` macro.

|DML_TARGET_VERSION|Effetto|
|-|-|
|`0x3000`|Tutte le funzionalità che richiedono una versione di DirectML successiva alla **1.4.0** sono escluse da `DirectML.h` .|
|`0x2000`|Tutte le funzionalità che richiedono una versione di DirectML successiva alla **1.1.0** sono escluse da `DirectML.h` .|
|`0x1000`|Tutte le funzionalità che richiedono una versione di DirectML successiva alla **1.0.0** sono escluse da `DirectML.h` .|
|*Non impostato*|La versione di destinazione viene selezionata automaticamente. Vedere di seguito per altri dettagli.|

Se `DML_TARGET_VERSION` non è impostato, viene selezionato automaticamente come segue.

* Se la `DML_TARGET_VERSION_USE_LATEST` macro è definita, viene selezionata la versione di destinazione più recente.
* In caso contrario, la versione di destinazione viene selezionata in base al valore della `NTDDI_VERSION` macro.
  *  `NTDDI_WIN10_19H1` comporta una versione di destinazione di `0x1000` .
  *  `NTDDI_WIN10_VB` comporta una versione di destinazione di `0x2000` .
  *  Se non è definito, viene selezionata la versione di destinazione più recente `NTDDI_VERSION` (come `DML_TARGET_VERSION_USE_LATEST` se fosse specificata).

### <a name="example"></a>Esempio

Si consideri un'applicazione che usa la versione 10.0.19041.0 (Windows 10, versione 2004) di Windows Software Development Kit (Windows SDK) (SDK). Dalla tabella precedente, la versione di DirectML a cui corrisponde è 1.1.0 e la corrispondente `DML_TARGET_VERSION` è `0x2000` .

Se non si impostano né le macro , la versione di destinazione selezionata verrà impostata per impostazione predefinita su e tutti gli elementi in saranno `DML_TARGET_VERSION` `NTDDI_VERSION` disponibili per `0x2000` `DirectML.h` l'uso.

Se si vuole che l'applicazione possa essere eseguita Windows 10, versione 1903 (10.0; Build 18362), è quindi possibile , che escluderà tutto il contenuto in che non `#define DML_TARGET_VERSION 0x1000` `DirectML.h` è supportato da DirectML versione 1.0.0. In questo modo si garantisce che qualsiasi tentativo di usare funzionalità che richiede una versione maggiore non venga compilato.

## <a name="directml-version-versus-feature-level"></a>Versione di DirectML rispetto al livello di funzionalità

La versione DirectML (ad esempio, 1.0.0 o 1.4.0) descrive una particolare versione di DirectML, inclusi il file di intestazione e il `DirectML.h` `.lib` file associati.

Il livello di funzionalità ( ad esempio , o ) descrive la funzionalità dell'implementazione sottostante dell'API, che può variare rispetto `DML_FEATURE_LEVEL_1_0` `DML_FEATURE_LEVEL_2_0` alla versione di `DirectML.h` usata.

Ad esempio, un'applicazione compilata su un SDK più recente, ma in esecuzione in una versione precedente di Windows, potrebbe (in fase di esecuzione) vedere un livello di funzionalità supportato inferiore, anche se viene compilato con l'SDK più recente.

## <a name="see-also"></a>Vedi anche

* [Cronologia a livello di funzionalità DirectML](./dml-feature-level-history.md)
* [DML_FEATURE_LEVEL enumerazione](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Pacchetto ridistribuibile Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)