---
title: Cronologia delle versioni di DirectML
description: DirectML viene distribuito come componente di sistema di Windows 10 ed è disponibile come parte del sistema operativo Windows 10 (sistema operativo) in Windows 10, versione 1903 (10,0; Build 18362) e versioni successive.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 04cb7a2c906d7674c793a9a99e21609ea874dbc1
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104548909"
---
# <a name="directml-version-history"></a>Cronologia delle versioni di DirectML

DirectML viene distribuito come componente di sistema di Windows 10 ed è disponibile come parte del sistema operativo Windows 10 (sistema operativo) in Windows 10, versione 1903 (10,0; Build 18362) e versioni successive.

A partire da DirectML versione 1.4.0, DirectML è disponibile anche come pacchetto ridistribuibile autonomo (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/)), che è utile per le applicazioni che vogliono usare una versione fissa di DirectML o quando eseguono versioni precedenti di Windows 10.

DirectML segue le convenzioni di [controllo delle versioni semantiche](https://semver.org/) . Ovvero i numeri di versione seguono il modulo `major.minor.patch` . La prima versione di DirectML è la versione 1.0.0.

## <a name="version-table"></a>Tabella della versione

|Versione di DirectML|Livello di funzionalità supportato (vedere la [cronologia a livello di funzionalità di DirectML](./dml-feature-level-history.md))|DML_TARGET_VERSION|Disponibile per la prima volta in|Primo disponibile in (ridistribuibile)|
|-|-|-|-|-|-|
|1.4.0<sup>1</sup>|DML_FEATURE_LEVEL_3_0|`0x3000`|N/D|[DirectML-1.4.0](https://www.nuget.org/packages/Microsoft.AI.DirectML/)|
|1.1.0|DML_FEATURE_LEVEL_2_0|`0x2000`|Windows 10, versione 2004 (10,0; Compilazione 19041) (aggiornamento di Windows 10 maggio 2020). Noto come "20H1".|N/D|
|1.0.0|DML_FEATURE_LEVEL_1_0|`0x1000`|Windows 10, versione 1903 (10,0; Compilazione 18362) (aggiornamento di Windows 10 maggio 2019). Noto come "19H1".|N/D|

<sup>1</sup> le versioni intermedie 1.2.0 e 1.3.0 di DirectML non sono state rese disponibili a livello generale.

## <a name="selecting-a-directml-target-version"></a>Selezione di una versione di destinazione di DirectML

Per praticità, alcune funzionalità nel `DirectML.h` file di intestazione vengono dichiarate in modo condizionale in base al valore della `DML_TARGET_VERSION` macro. Impostando la `DML_TARGET_VERSION` macro su determinati valori, è possibile escludere parti di `DirectML.h` dall'applicazione.

Questa operazione può essere utile se si usa una copia più recente di `DirectML.h` , ma si sta impostando come destinazione una versione precedente del file binario DirectML, perché assicura che qualsiasi tentativo di usare le funzionalità oltre il livello di destinazione scelto non venga compilato. Questo meccanismo è simile alla `NTDDI_VERSION` macro (vedere [macro per le dichiarazioni condizionali](../winprog/using-the-windows-headers.md#macros-for-conditional-declarations)).

Di seguito sono riportati i valori validi per la `DML_TARGET_VERSION` macro.

|DML_TARGET_VERSION|Effetto|
|-|-|
|`0x3000`|Tutte le funzionalità che richiedono una versione di DirectML più recente di **1.4.0** sono escluse da `DirectML.h` .|
|`0x2000`|Tutte le funzionalità che richiedono una versione di DirectML più recente di **1.1.0** sono escluse da `DirectML.h` .|
|`0x1000`|Tutte le funzionalità che richiedono una versione di DirectML più recente di **1.0.0** sono escluse da `DirectML.h` .|
|*Non impostato*|La versione di destinazione viene selezionata automaticamente. Vedere di seguito per altri dettagli.|

Se `DML_TARGET_VERSION` non è impostato, viene selezionato automaticamente in base a quanto segue.

* Se la `DML_TARGET_VERSION_USE_LATEST` macro è definita, viene selezionata la versione di destinazione più recente.
* In caso contrario, la versione di destinazione viene selezionata in base al valore della `NTDDI_VERSION` macro.
  *  `NTDDI_WIN10_19H1` Restituisce una versione di destinazione di `0x1000` .
  *  `NTDDI_WIN10_VB` Restituisce una versione di destinazione di `0x2000` .
  *  Se `NTDDI_VERSION` non è definito, viene selezionata la versione di destinazione più recente (come se `DML_TARGET_VERSION_USE_LATEST` fosse specificato).

### <a name="example"></a>Esempio

Si consideri un'applicazione che usa la versione 10.0.19041.0 (Windows 10, versione 2004) di Windows Software Development Kit (SDK). Dalla tabella precedente, la versione di DirectML che corrisponde a è 1.1.0 e l'oggetto corrispondente `DML_TARGET_VERSION` è `0x2000` .

Se non si impostano le `DML_TARGET_VERSION` `NTDDI_VERSION` macro, la versione di destinazione selezionata verrà impostata automaticamente su `0x2000` e tutti gli elementi in `DirectML.h` saranno disponibili per l'utilizzo.

Se si vuole che l'applicazione possa essere eseguita in Windows 10, versione 1903 (10,0; Build 18362), quindi è possibile `#define DML_TARGET_VERSION 0x1000` , che esclude tutto il contenuto in `DirectML.h` che non è supportato da DirectML versione 1.0.0. In questo modo si garantisce che qualsiasi tentativo di utilizzare la funzionalità che richiede una versione successiva non riuscirà a compilare.

## <a name="directml-version-versus-feature-level"></a>Versione di DirectML rispetto a livello di funzionalità

La versione di DirectML (ad esempio 1.0.0 o 1.4.0) descrive una versione specifica di DirectML, inclusi il file di `DirectML.h` intestazione e il `.lib` file associati.

Il livello di funzionalità, ad esempio, `DML_FEATURE_LEVEL_1_0` o, `DML_FEATURE_LEVEL_2_0` descrive la funzionalità dell'implementazione sottostante dell'API, che può variare dalla versione di `DirectML.h` usata.

Ad esempio, un'applicazione che si basa su un SDK più recente, ma in esecuzione su una versione precedente di Windows, potrebbe (in fase di esecuzione) vedere un livello di funzionalità supportato inferiore, anche se viene compilato con l'SDK più recente.

## <a name="see-also"></a>Vedi anche

Cronologia a livello di [funzionalità DirectML](./dml-feature-level-history.md) 
 [Enumerazione DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) 
 [Microsoft. ai. DirectML Redistributable Package](https://www.nuget.org/packages/Microsoft.AI.DirectML/)