---
description: È simile a un'opzione della riga di comando. Tuttavia, non è necessario immettere nuovamente un \# comando pragma ogni volta che si compila un file MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317581"
---
# <a name="pragma"></a>\#pragma

Il comando per il preprocessore **\# pragma** è simile a un'opzione della riga di comando. Tuttavia, non è necessario immettere nuovamente un comando **\# pragma** ogni volta che si compila un file MOF. Nell'esempio seguente viene illustrata la sintassi del comando **\# pragma** :


```mof
#pragma [command]
```



In genere si inserisce un comando **\# pragma** all'inizio di un file MOF. Tuttavia, è possibile inserire alcuni comandi, ad esempio il comando **\# pragma** , nel corpo del codice MOF. Nell'esempio seguente vengono illustrati i comandi **\# pragma** che indicano al compilatore MOF che deve inserire classi e istanze nello \\ spazio dei nomi CIMV2 radice e compilare il file in cui sono inclusi i comandi durante il ripristino del repository:


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



Di seguito sono elencati i comandi **\# pragma** disponibili.



| Comando                                         | Descrizione                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**emendamento**](pragma-amendment.md)           | Indica al compilatore MOF di separare un file MOF in versioni indipendenti dalla lingua e dal linguaggio. |
| [**salvataggio automatico**](pragma-autorecover.md)       | Aggiunge un file MOF all'elenco di file compilati durante il ripristino del repository.                             |
| [**classFlags**](pragma-classflags.md)         | Controlla il modo in cui le classi vengono create o aggiornate a seconda dei flag specificati.                     |
| [**deleteclass**](pragma-deleteclass.md)       | Elimina una classe esistente e le relative istanze dal repository.                                      |
| [**DeleteInstance**](pragma-deleteinstance.md) | Elimina un'istanza esistente di una classe dal repository.                                          |
| [**instanceflags**](pragma-instanceflags.md)   | Controlla il modo in cui le istanze vengono create o aggiornate a seconda dei flag specificati.                   |
| [**namespace**](pragma-namespace.md)           | Richiede che il compilatore carichi il file MOF nello spazio dei nomi specificato come *namespacePath*.         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



