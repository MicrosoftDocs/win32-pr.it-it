---
description: È simile a un'opzione della riga di comando. Tuttavia, non è necessario reim eseguire di nuovo un \# comando pragma ogni volta che si compila un file MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3cb9541ceef51119ce521244282920ca88397afe13290e99bdc14ce7d98ab55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860561"
---
# <a name="pragma"></a>\#pragma

Il **\# comando del** preprocessore pragma è simile a un'opzione della riga di comando. Tuttavia, non è necessario reim eseguire di nuovo un **\# comando pragma** ogni volta che si compila un file MOF. L'esempio seguente illustra la sintassi **\# dei comandi pragma:**


```mof
#pragma [command]
```



In genere si posiziona un **\# comando pragma** all'inizio di un file MOF. Tuttavia, è possibile inserire alcuni comandi, ad esempio il **\# comando pragma,** nel corpo del codice MOF. L'esempio seguente illustra i comandi **\# pragma** che indicano al compilatore MOF che devono inserire classi e istanze nello spazio dei nomi cimv2 radice e compilare il file in cui sono inclusi i comandi durante il ripristino del \\ repository:


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



Di seguito sono elencati i comandi **\# pragma** disponibili.



| Comando                                         | Descrizione                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Emendamento**](pragma-amendment.md)           | Indica al compilatore MOF di separare un file MOF in versioni indipendenti dalla lingua e specifiche del linguaggio. |
| [**Automaticamente**](pragma-autorecover.md)       | Aggiunge un file MOF all'elenco di file compilati durante il ripristino del repository.                             |
| [**classflags**](pragma-classflags.md)         | Controlla il modo in cui le classi vengono create o aggiornate a seconda dei flag specificati.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Elimina una classe esistente e le relative istanze dal repository.                                      |
| [**deleteinstance**](pragma-deleteinstance.md) | Elimina un'istanza esistente di una classe dal repository.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Controlla la modalità di creazione o aggiornamento delle istanze a seconda dei flag specificati.                   |
| [**Namespace**](pragma-namespace.md)           | Richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come *namespacepath*.         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comandi per il preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



