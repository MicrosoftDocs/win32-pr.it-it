---
description: 'Altre informazioni su: parametri di sistema Extensible Storage Engine'
title: Parametri di sistema Extensible Storage Engine
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
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527990"
---
# <a name="extensible-storage-engine-system-parameters"></a>Parametri di sistema Extensible Storage Engine


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine-system-parameters"></a>Parametri di sistema Extensible Storage Engine

Le costanti seguenti vengono usate come valori per il parametro *Paramid* delle funzioni [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) .

  - [Parametri di backup e ripristino](./backup-and-restore-parameters.md)

  - [Parametri di callback](./callback-parameters.md)

  - [Parametri del database](./database-parameters.md)

  - [Parametri della cache del database](./database-cache-parameters.md)

  - [Parametri di gestione degli errori](./error-handling-parameters.md)

  - [Parametri del registro eventi](./event-log-parameters.md)

  - [Parametri di I/O](./i-o-parameters.md)

  - [Parametri dell'indice](./index-parameters.md)

  - [Parametri informativi](./informational-parameters.md)

  - [Meta parametri](./meta-parameters.md)

  - [Parametri delle risorse](./resource-parameters.md)

  - [Parametri di database temporanei](./temporary-database-parameters.md)

  - [Parametri del log delle transazioni](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Formato Descrizione parametro di sistema

Ogni parametro di sistema verrà descritto utilizzando il formato seguente:

JET_paramX

Descrizione del parametro di sistema JET_paramX.

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
<td><p>Il parametro è globale o per istanza?</p></td>
</tr>
<tr class="odd">
<td><p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>È possibile impostare il parametro se esistono istanze?</p></td>
</tr>
<tr class="even">
<td><p>Imposta dopo <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>È possibile impostare il parametro durante l'inizializzazione?</p></td>
</tr>
<tr class="odd">
<td><p>Influiscono sul layout fisico:</p></td>
<td><p>Il parametro influisce sui file su disco?</p></td>
</tr>
<tr class="even">
<td><p>Influire sull'affidabilità:</p></td>
<td><p>Il parametro influisce sull'affidabilità del motore?</p></td>
</tr>
<tr class="odd">
<td><p>Influire sulle prestazioni:</p></td>
<td><p>Il parametro influisce sulle prestazioni del motore?</p></td>
</tr>
<tr class="even">
<td><p>Influiscono sulle risorse:</p></td>
<td><p>Il parametro influisce sulle risorse del motore?</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilità:</p></td>
<td><p>Versioni di Windows che supportano il parametro.</p></td>
</tr>
</tbody>
</table>
