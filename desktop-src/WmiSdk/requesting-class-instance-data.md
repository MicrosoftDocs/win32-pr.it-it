---
description: 'Le query sui dati sono istruzioni WQL che richiedono istanze di classi. Per eseguire una query di dati, le applicazioni chiamano il metodo IWbemServices:: ExecQuery o IWbemServices:: ExecQueryAsync.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Richiesta di dati dell'istanza di classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32df053ae1267f396978d98271f57f174ea6bf0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318536"
---
# <a name="requesting-class-instance-data"></a><span data-ttu-id="47e70-104">Richiesta di dati dell'istanza di classe</span><span class="sxs-lookup"><span data-stu-id="47e70-104">Requesting Class Instance Data</span></span>

<span data-ttu-id="47e70-105">Le query sui dati sono istruzioni WQL che richiedono istanze di classi.</span><span class="sxs-lookup"><span data-stu-id="47e70-105">Data queries are WQL statements that request instances of classes.</span></span> <span data-ttu-id="47e70-106">Per eseguire una query di dati, le applicazioni chiamano il metodo [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) o [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="47e70-106">To issue a data query, applications call the [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) or [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method.</span></span>

<span data-ttu-id="47e70-107">Per eseguire query sui dati, vengono utilizzate le istruzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="47e70-107">The following statements are used to make data queries:</span></span>

-   [<span data-ttu-id="47e70-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="47e70-108">SELECT</span></span>](select-statement-for-data-queries.md)
-   [<span data-ttu-id="47e70-109">ASSOCIATORI DI</span><span class="sxs-lookup"><span data-stu-id="47e70-109">ASSOCIATORS OF</span></span>](associators-of-statement.md)
-   [<span data-ttu-id="47e70-110">RIFERIMENTI DI</span><span class="sxs-lookup"><span data-stu-id="47e70-110">REFERENCES OF</span></span>](references-of-statement.md)
-   [<span data-ttu-id="47e70-111">ISA</span><span class="sxs-lookup"><span data-stu-id="47e70-111">ISA</span></span>](isa-operator-for-data-queries.md)

<span data-ttu-id="47e70-112">L'istruzione di selezione WQL è l'istruzione Structured Query Language standard (SQL) per il recupero di informazioni, con alcune restrizioni ed estensioni specifiche di WQL.</span><span class="sxs-lookup"><span data-stu-id="47e70-112">The WQL SELECT statement is the standard Structured Query Language (SQL) statement for retrieving information, with a few restrictions and extensions specific to WQL.</span></span> <span data-ttu-id="47e70-113">Sebbene l'istruzione SQL SELECT venga in genere utilizzata nell'ambiente di database per recuperare colonne specifiche dalle tabelle, in WMI viene utilizzata l'istruzione di selezione WQL per recuperare le istanze di una singola classe.</span><span class="sxs-lookup"><span data-stu-id="47e70-113">Although the SQL SELECT statement is typically used in the database environment to retrieve particular columns from tables, the WQL SELECT statement is used in WMI to retrieve instances of a single class.</span></span> <span data-ttu-id="47e70-114">WQL non supporta le query su più classi.</span><span class="sxs-lookup"><span data-stu-id="47e70-114">WQL does not support queries across multiple classes.</span></span>

<span data-ttu-id="47e70-115">Gli ASSOCIATOri di e i riferimenti di istruzioni sono specifici di WQL e non fanno parte di SQL standard.</span><span class="sxs-lookup"><span data-stu-id="47e70-115">The ASSOCIATORS OF and REFERENCES OF statements are specific to WQL and are not part of standard SQL.</span></span> <span data-ttu-id="47e70-116">L'ASSOCIAZIONErs OF Statement recupera tutte le istanze di classe associate a una particolare istanza della classe di origine e i riferimenti di recupera tutte le istanze che fanno riferimento a una particolare istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="47e70-116">The ASSOCIATORS OF statement retrieves all class instances that are associated with a particular source class instance, and REFERENCES OF retrieves all instances that refer to a particular source instance.</span></span> <span data-ttu-id="47e70-117">Le associazioni sono rappresentate da istanze di una [classe di associazione](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="47e70-117">Associations are represented by instances of an [association class](declaring-an-association-class.md).</span></span>

 

 



