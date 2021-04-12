---
description: Una sequenza di finestra di dialogo FirstRun raccoglie il nome utente, il nome della società e le informazioni sull'ID prodotto. Il programma di installazione verifica l'ID prodotto durante la finestra di dialogo.
ms.assetid: bb77296f-705a-4409-b2ca-a76bbaf7ea57
title: Finestra di dialogo FirstRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2024683d7a10395340a18ddd2015b94e1207bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226618"
---
# <a name="firstrun-dialog"></a><span data-ttu-id="1ee03-104">Finestra di dialogo FirstRun</span><span class="sxs-lookup"><span data-stu-id="1ee03-104">FirstRun Dialog</span></span>

<span data-ttu-id="1ee03-105">Una sequenza di finestra di dialogo FirstRun raccoglie il nome utente, il nome della società e le informazioni sull'ID prodotto.</span><span class="sxs-lookup"><span data-stu-id="1ee03-105">A FirstRun dialog box sequence collects user name, company name, and product ID information.</span></span> <span data-ttu-id="1ee03-106">Il programma di installazione verifica l'ID prodotto durante la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1ee03-106">The installer verifies the product ID during this dialog.</span></span>

<span data-ttu-id="1ee03-107">Una sequenza della finestra di dialogo FirstRun non fa in genere parte della sequenza di azione e viene invece chiamata dalla funzione [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) alla prima esecuzione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="1ee03-107">A FirstRun dialog box sequence is usually not a part of the action sequence and is instead called by the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function on the first run of the product.</span></span>

<span data-ttu-id="1ee03-108">Un autore di un pacchetto del programma di installazione può utilizzare la sequenza della finestra di dialogo modello o creare una sequenza diversa.</span><span class="sxs-lookup"><span data-stu-id="1ee03-108">An author of an installer package may use the template dialog sequence or create a different sequence.</span></span> <span data-ttu-id="1ee03-109">La sequenza della finestra di dialogo richiede tuttavia che l'utente abbia impostato le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ee03-109">The dialog sequence however needs to have the user set the following properties:</span></span>

-   <span data-ttu-id="1ee03-110">[**Username**](username.md) (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1ee03-110">[**USERNAME**](username.md) property</span></span>
-   <span data-ttu-id="1ee03-111">[**CompanyName**](companyname.md) (proprietà)</span><span class="sxs-lookup"><span data-stu-id="1ee03-111">[**COMPANYNAME**](companyname.md) property</span></span>
-   <span data-ttu-id="1ee03-112">Proprietà [**codice PIDKEY**](pidkey.md)</span><span class="sxs-lookup"><span data-stu-id="1ee03-112">[**PIDKEY**](pidkey.md) property</span></span>

<span data-ttu-id="1ee03-113">L'ID prodotto verrà convalidato durante la finestra di dialogo mediante l' [azione ValidateProductID](validateproductid-action.md) o [ValidateProductID ControlEvent](validateproductid-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="1ee03-113">The product ID will be validated during the dialog using the [ValidateProductID action](validateproductid-action.md) or the [ValidateProductID ControlEvent](validateproductid-controlevent.md).</span></span>

<span data-ttu-id="1ee03-114">Se l'ID prodotto è impostato come proprietà nella riga di comando o da una trasformazione, è necessario che l'utente immetta nuovamente l'ID prodotto durante la finestra di dialogo di prima esecuzione possa essere eluso controllando la visualizzazione utilizzando la proprietà [**ProductID**](productid.md) .</span><span class="sxs-lookup"><span data-stu-id="1ee03-114">If the product ID is set as a property on the command line, or by a transform, then the necessity of having the user reenter the product ID during the first-run dialog can be circumvented by controlling the display using the [**ProductID**](productid.md) property.</span></span> <span data-ttu-id="1ee03-115">Dopo la corretta convalida dell'ID prodotto, la proprietà **ProductID** è impostata sull'ID prodotto completo e valido.</span><span class="sxs-lookup"><span data-stu-id="1ee03-115">Following the successful validation of the product ID the **ProductID** property is set to the full, valid product ID.</span></span>

 

 



