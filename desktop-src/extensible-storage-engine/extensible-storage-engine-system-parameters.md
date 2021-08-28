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
ms.openlocfilehash: 501f98ec1b360e3eaa10988c140f30b86dcacb5a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987344"
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


| Etichetta | Valore |
|--------|-------|
| <p>Valore predefinito:</p> | <p>Valore predefinito del parametro.</p> | 
| <p>Digitare:</p> | <p>Tipo di dati del parametro.</p> | 
| <p>Intervallo valido:</p> | <p>Valori validi per il parametro.</p> | 
| <p>Ambito:</p> | <p>Il parametro è Globale o per istanza?</p> | 
| <p>Imposta dopo <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>È possibile impostare il parametro se sono presenti istanze?</p> | 
| <p>Impostato dopo <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>È possibile impostare il parametro quando viene inizializzato?</p> | 
| <p>Influisce sul layout fisico:</p> | <p>Il parametro influisce sui file su disco?</p> | 
| <p>Influisce sull'affidabilità:</p> | <p>Il parametro influisce sull'affidabilità del motore?</p> | 
| <p>Influisce sulle prestazioni:</p> | <p>Il parametro influisce sulle prestazioni del motore?</p> | 
| <p>Influisce sulle risorse:</p> | <p>Il parametro influisce sulle risorse del motore?</p> | 
| <p>Disponibilità:</p> | <p>Versioni di Windows che supportano il parametro .</p> | 

