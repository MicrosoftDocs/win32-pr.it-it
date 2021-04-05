---
description: "Altre informazioni su: colonne definite dall'utente"
title: Colonne definite dall'utente
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049741"
---
# <a name="user-defined-columns"></a><span data-ttu-id="f4359-103">Colonne definite dall'utente</span><span class="sxs-lookup"><span data-stu-id="f4359-103">User Defined Columns</span></span>


<span data-ttu-id="f4359-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f4359-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="user-defined-columns"></a><span data-ttu-id="f4359-105">Colonne definite dall'utente</span><span class="sxs-lookup"><span data-stu-id="f4359-105">User Defined Columns</span></span>

<span data-ttu-id="f4359-106">Le colonne definite dall'utente sono colonne i cui valori predefiniti sono forniti da una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f4359-106">User defined columns are columns whose default values are provided by a callback function.</span></span> <span data-ttu-id="f4359-107">Queste colonne vengono sempre contrassegnate e impostate sul valore calcolato dalla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="f4359-107">These columns are always tagged and set to the value computed by the callback function.</span></span> <span data-ttu-id="f4359-108">Questo valore deve essere stabile per ogni riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="f4359-108">This value must be stable for each row in the table.</span></span> <span data-ttu-id="f4359-109">La funzione di callback viene utilizzata solo quando il motore di database o l'applicazione deve leggere il valore della colonna per una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="f4359-109">The callback function is only used when either the application or the database engine itself needs to read the value of the column for a given row.</span></span> <span data-ttu-id="f4359-110">Nell'applicazione è possibile eseguire l'override del valore predefinito e impostare un valore specifico nella colonna.</span><span class="sxs-lookup"><span data-stu-id="f4359-110">The application has the option to override the default value and set a specific value in the column.</span></span> <span data-ttu-id="f4359-111">Quando si esegue l'override del valore predefinito nelle colonne, viene utilizzato lo spazio nella riga; in caso contrario, le colonne predefinite definite dall'utente non utilizzano lo spazio nel record.</span><span class="sxs-lookup"><span data-stu-id="f4359-111">When the default value is overridden in the columns, it uses space in the row, otherwise user defined default columns do not use space in the record.</span></span>

<span data-ttu-id="f4359-112">L'opzione impostazioni predefinite definite dall'utente è impostata nel membro **grbit** della struttura [JET_COLUMNDEF](./jet-columndef-structure.md) nella chiamata a [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="f4359-112">User defined defaults option is set in the **grbit** member of the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="f4359-113">Il parametro *pvDefault* della funzione [JetAddColumn](./jetaddcolumn-function.md) punta a una struttura di [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , che contiene il nome della funzione di callback nel membro **szCallback** e i dati passati al callback nel membro **pbUserData** .</span><span class="sxs-lookup"><span data-stu-id="f4359-113">The *pvDefault* parameter of the [JetAddColumn](./jetaddcolumn-function.md) function points to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure, that contains the name of the callback function in the **szCallback** member, and the data that is passed to the callback in the **pbUserData** member.</span></span>
