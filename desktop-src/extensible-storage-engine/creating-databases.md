---
description: 'Altre informazioni su: creazione di database'
title: Creazione di database
TOCTitle: Creating Databases
ms:assetid: d221144d-f777-4f8a-80ca-2ebdb77108dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294100(v=EXCHG.10)
ms:contentKeyID: 32765715
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eac708b64837fc79fa8a5060df7deb93ec552e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308553"
---
# <a name="creating-databases"></a>Creazione di database


_**Si applica a:** Windows | Windows Server_

## <a name="creating-databases"></a>Creazione di database

Il database ESE è costituito da una o più tabelle che organizzano i dati per colonne e righe. Il database ESE viene identificato in base al nome e all'ID del database. Un database ESE è simile a un singolo file nel sistema operativo Microsoft Windows; Tuttavia, internamente il database viene archiviato come raccolta di pagine. Queste pagine contengono metadati che descrivono i dati nel database, i dati stessi e uno o più indici che archiviano ordini diversi dei dati. Il database può contenere fino a 2 ^ 31 pagine o 16 terabyte di dati per un database con pagine da 8 KB.

L'applicazione crea un'istanza del motore di database, quindi crea un database e lo connette all'istanza di. È possibile collegare fino a 6 database contemporaneamente a un'istanza di con [JetCreateDatabase](./jetcreatedatabase-function.md) o [JetAttachDatabase](./jetattachdatabase-function.md). È necessario avviare una o più sessioni all'interno del database, perché tutte le operazioni ESE successive vengono eseguite nel contesto di una sessione. È necessario aprire una sessione separata per ogni thread utilizzando ESE.

Tramite questa procedura verrà inizializzato ESE e verrà creato un database.

### <a name="to-initialize-ese-and-create-a-database"></a>Per inizializzare ESE e creare un database

1.  [JetCreateInstance](./jetcreateinstance-function.md): crea un'istanza del motore di database.
    
    **Windows XP e versioni successive:** Questa funzione è disponibile in Windows XP e versioni successive. In Windows 2000 è supportata una sola istanza e tale istanza viene creata in modo implicito

2.  [JetSetSystemParameter](./jetsetsystemparameter-function.md): i parametri di sistema che hanno effetto sul layout fisico, ad esempio JET_paramLogFilePath e JET_paramSystemPath, devono essere impostati prima di inizializzare l'istanza con [JetInit](./jetinit-function.md). I parametri impostati in questa fase vengono impostati per tutti i database creati nell'istanza. [JetSetSystemParameter](./jetsetsystemparameter-function.md) è l'unica funzione che può utilizzare l'istanza prima che venga inizializzata con [JetInit](./jetinit-function.md).

3.  [JetInit](./jetinit-function.md): Inizializza l'istanza di. L'istanza deve essere inizializzata con [JetInit](./jetinit-function.md) prima di poter essere usata con qualsiasi altra funzione.

4.  [JetBeginSession](./jetbeginsession-function.md): crea la sessione per tutte le transazioni successive. Tutte le transazioni di database si verificano nel contesto della sessione ([JET_SESID](./jet-sesid.md)).

5.  [JetCreateDatabase](./jetcreatedatabase-function.md): crea il database e restituisce un handle per l'ID del database ([JET_DBID](./jet-dbid.md)).
    
    Se il database esiste già, il passaggio 5 precedente viene sostituito dai due passaggi seguenti:
    
    1.  [JetAttachDatabase](./jetattachdatabase-function.md): connette il database in base al nome alla sessione
    
    2.  [JetOpenDatabase](./jetopendatabase-function.md): restituisce l'ID del database utilizzato nelle operazioni di database successive.

Un database può essere scollegato da un'istanza ESE utilizzando [JetDetachDatabase](./jetdetachdatabase-function.md) e successivamente collegato a un'altra istanza con [JetAttachDatabase](./jetattachdatabase-function.md). Quando il database viene scollegato, è possibile copiarlo come singolo file utilizzando le utilità standard di Windows. Tuttavia, quando il database viene collegato a un'istanza di ESE, non può essere copiato perché ESE apre esclusivamente i file di database. Inoltre, se l'istanza si arresta in modo anomalo, il file di database non può essere copiato da solo perché è necessario che i file di log delle transazioni siano associati per il ripristino da tale arresto anomalo.
