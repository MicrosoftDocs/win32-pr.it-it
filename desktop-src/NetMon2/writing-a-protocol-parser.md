---
description: Questo argomento contiene informazioni sulla scrittura di un parser di protocollo e include esempi delle funzioni di esportazione che devono essere implementate dalla DLL del parser.
ms.assetid: 0be87b33-aab0-4986-8a86-914e0a7b8f2d
title: Scrittura di un parser di protocollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338c224dd036df747af6ab805dae273f6ad3f510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528734"
---
# <a name="writing-a-protocol-parser"></a><span data-ttu-id="50f7c-103">Scrittura di un parser di protocollo</span><span class="sxs-lookup"><span data-stu-id="50f7c-103">Writing a Protocol Parser</span></span>

<span data-ttu-id="50f7c-104">Questo argomento contiene informazioni sulla scrittura di un parser di protocollo e include esempi delle funzioni di esportazione che devono essere implementate dalla DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="50f7c-104">This topic contains information about writing a protocol parser, and includes examples of the export functions that the parser DLL must implement.</span></span>

<span data-ttu-id="50f7c-105">In questa sezione sono inclusi gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="50f7c-105">The following topics are included in this section.</span></span>



| <span data-ttu-id="50f7c-106">Termine</span><span class="sxs-lookup"><span data-stu-id="50f7c-106">Term</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="50f7c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50f7c-107">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f7c-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Considerazioni sulla programmazione](programming-considerations.md)</span><span class="sxs-lookup"><span data-stu-id="50f7c-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Programming Considerations](programming-considerations.md)</span></span><br/>                                                   | <span data-ttu-id="50f7c-109">Identifica i suggerimenti per la programmazione di base che consentono di scrivere una DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="50f7c-109">Identifies the basic programming tips to help you write a parser DLL.</span></span><br/>                                                                                    |
| <span data-ttu-id="50f7c-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementazione di funzioni di esportazione del parser](implementing-parser-export-functions.md)</span><span class="sxs-lookup"><span data-stu-id="50f7c-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementing Parser Export Functions](implementing-parser-export-functions.md)</span></span><br/> | <span data-ttu-id="50f7c-111">Fornisce esempi di implementazione di funzioni di esportazione.</span><span class="sxs-lookup"><span data-stu-id="50f7c-111">Provides examples of implementing export functions.</span></span><br/>                                                                                                      |
| <span data-ttu-id="50f7c-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formattazione dei dati visualizzati](formatting-displayed-data.md)</span><span class="sxs-lookup"><span data-stu-id="50f7c-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatting Displayed Data](formatting-displayed-data.md)</span></span><br/>                                                        | <span data-ttu-id="50f7c-113">Identifica il processo di formattazione dei dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="50f7c-113">Identifies the process of formatting data that is displayed in the details pane of the Network Monitor UI.</span></span><br/>                                               |
| <span data-ttu-id="50f7c-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Specifica di un set di seguito](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="50f7c-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/>                                                                  | <span data-ttu-id="50f7c-115">Identifica il processo di definizione di un set di seguito e Mostra come Network Monitor accede al set di un parser seguente per determinare il protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="50f7c-115">Identifies the process of specifying a follow set, and shows you how Network Monitor accesses the follow set of a parser to determine the next protocol.</span></span><br/> |
| <span data-ttu-id="50f7c-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Specifica di un set di continuità](specifying-a-handoff-set.md)</span><span class="sxs-lookup"><span data-stu-id="50f7c-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Specifying a Handoff Set](specifying-a-handoff-set.md)</span></span><br/>                                                             | <span data-ttu-id="50f7c-117">Identifica il processo di specifica di un set di continuità e Mostra come il parser accede al set di continuità per ottenere un handle per il protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="50f7c-117">Identifies the process of specifying a handoff set, and shows you how the parser accesses its handoff set to get a handle to the next protocol.</span></span><br/>          |



 

 

 




