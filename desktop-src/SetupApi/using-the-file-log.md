---
description: Prima di poter usare un log di file, è necessario chiamare SetupInitializeFileLog per aprirlo o crearlo. Quando si chiama questa funzione, è possibile specificare i flag per creare o sovrascrivere un log di file, aprire il registro di sistema o aprire un log di file come di sola lettura.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Uso del file di log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968750"
---
# <a name="using-the-file-log"></a>Uso del file di log

Prima di poter usare un log di file, è necessario chiamare [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) per aprirlo o crearlo. Quando si chiama questa funzione, è possibile specificare i flag per creare o sovrascrivere un log di file, aprire il registro di sistema o aprire un log di file come di sola lettura.

Dopo che [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) restituisce un handle a un log file, è possibile aggiungere una voce chiamando [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), eliminare una voce chiamando [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)o recuperare informazioni su un determinato file in un log file chiamando [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).

Quando il log del file non è più necessario, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) deve essere chiamato per rilasciare le risorse allocate durante la chiamata a [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).

 

 



