---
description: 'Altre informazioni su: Extensible Archiviazione Engine System Parameters'
title: Extensible Archiviazione Engine System Parameters
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 531e599c66279312f80216f1eb09fc612636821227e76f3572645ab6b4ee5137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256448"
---
# <a name="extensible-storage-engine-system-parameters"></a>Extensible Archiviazione Engine System Parameters


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-system-parameters"></a>Extensible Archiviazione Engine System Parameters

Le costanti seguenti vengono usate come valori per il *parametro paramid* delle [funzioni JetGetSystemParameter](./jetgetsystemparameter-function.md) [e JetSetSystemParameter.](./jetsetsystemparameter-function.md)

  - [Parametri di backup e ripristino](./backup-and-restore-parameters.md)

  - [Parametri di callback](./callback-parameters.md)

  - [Parametri del database](./database-parameters.md)

  - [Parametri della cache del database](./database-cache-parameters.md)

  - [Parametri di gestione degli errori](./error-handling-parameters.md)

  - [Parametri del registro eventi](./event-log-parameters.md)

  - [Parametri di I/O](./i-o-parameters.md)

  - [Parametri dell'indice](./index-parameters.md)

  - [Parametri in informazioni](./informational-parameters.md)

  - [Meta Parameters](./meta-parameters.md)

  - [Parametri delle risorse](./resource-parameters.md)

  - [Parametri di database temporanei](./temporary-database-parameters.md)

  - [Parametri del log delle transazioni](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Formato della descrizione dei parametri di sistema

Ogni parametro di sistema verrà descritto usando il formato seguente:

JET_paramX

Descrizione del JET_paramX di sistema.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valore predefinito:</p></td>
<td><p>Valore predefinito del parametro.</p></td>
</tr>
<tr class="even">
<td><p>Digitare:</p></td>
<td><p>Tipo di dati del parametro.</p></td>
</tr>
<tr class="odd">
<td><p>Intervallo valido:</p></td>
<td><p>Valori validi per il parametro.</p></td>
</tr>
<tr class="even">
<td><p>Ambito:</p></td>
<td><p>Il parametro è Globale o per istanza?</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>È possibile impostare il parametro se sono presenti istanze?</p></td>
</tr>
<tr class="even">
<td><p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>È possibile impostare il parametro quando viene inizializzato?</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sul layout fisico:</p></td>
<td><p>Il parametro influisce sui file su disco?</p></td>
</tr>
<tr class="even">
<td><p>Influisce sull'affidabilità:</p></td>
<td><p>Il parametro influisce sull'affidabilità del motore?</p></td>
</tr>
<tr class="odd">
<td><p>Influisce sulle prestazioni:</p></td>
<td><p>Il parametro influisce sulle prestazioni del motore?</p></td>
</tr>
<tr class="even">
<td><p>Influisce sulle risorse:</p></td>
<td><p>Il parametro influisce sulle risorse del motore?</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Versioni di Windows che supportano il parametro .</p></td>
</tr>
</tbody>
</table>
