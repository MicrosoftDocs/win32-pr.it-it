---
description: Prima che le funzioni di installazione possano accedere alle informazioni nel file INF, è necessario aprirlo con una chiamata alla funzione SetupOpenInfFile. Questa funzione restituisce un handle per il file INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Apertura e chiusura di un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529323"
---
# <a name="opening-and-closing-an-inf-file"></a><span data-ttu-id="50722-104">Apertura e chiusura di un file INF</span><span class="sxs-lookup"><span data-stu-id="50722-104">Opening and Closing an INF file</span></span>

<span data-ttu-id="50722-105">Prima che le funzioni di installazione possano accedere alle informazioni nel file INF, è necessario aprirlo con una chiamata alla funzione [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) .</span><span class="sxs-lookup"><span data-stu-id="50722-105">Before the setup functions can access information in the INF, you must open it with a call to the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function.</span></span> <span data-ttu-id="50722-106">Questa funzione restituisce un handle per il file INF.</span><span class="sxs-lookup"><span data-stu-id="50722-106">This function returns a handle to the INF file.</span></span>

<span data-ttu-id="50722-107">Se non si conosce il nome del file INF che è necessario aprire, è possibile utilizzare la funzione [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) per ottenere un elenco di file inf in una directory.</span><span class="sxs-lookup"><span data-stu-id="50722-107">If you do not know the name of the INF file that you need to open, you can use the [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) function to obtain a list of INF files in a directory.</span></span>

<span data-ttu-id="50722-108">Dopo aver aperto un file INF, è possibile aggiungere altri file INF al file INF aperto utilizzando la funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) .</span><span class="sxs-lookup"><span data-stu-id="50722-108">After you open an INF file, you can append additional INF files to the opened INF file by using the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function.</span></span> <span data-ttu-id="50722-109">Il funzionamento è simile a quello di un'istruzione di inclusione.</span><span class="sxs-lookup"><span data-stu-id="50722-109">This is functionally similar to an include statement.</span></span> <span data-ttu-id="50722-110">Quando le funzioni di installazione successive fanno riferimento a un file INF aperto, saranno anche in grado di accedere a tutte le informazioni archiviate nei file accodati.</span><span class="sxs-lookup"><span data-stu-id="50722-110">When subsequent setup functions reference an open INF file, they will also be able to access any information stored in the appended files.</span></span>

<span data-ttu-id="50722-111">Se non si specifica un file INF durante la chiamata alla funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , **SetupOpenAppendInfFile** aggiunge i file specificati dalla chiave **LayoutFile** nella sezione **Version** del file inf aperto.</span><span class="sxs-lookup"><span data-stu-id="50722-111">If you do not specify an INF file during the call to the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function, **SetupOpenAppendInfFile** appends the file(s) specified by the **LayoutFile** key in the **Version** section of the open INF file.</span></span>

<span data-ttu-id="50722-112">Quando non sono più necessarie le informazioni nel file INF, chiamare la funzione [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) per rilasciare le risorse allocate durante la chiamata a [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span><span class="sxs-lookup"><span data-stu-id="50722-112">When you no longer need the information in the INF file, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function to release resources allocated during the call to [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span></span>

 

 



