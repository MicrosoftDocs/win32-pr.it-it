---
title: Libri telefonici RAS
description: Le rubriche telefoniche forniscono un modo standard per raccogliere e specificare le informazioni necessarie alla gestione connessione di accesso remoto per stabilire una connessione remota.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Libri telefonici, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044813"
---
# <a name="ras-phone-books"></a><span data-ttu-id="81106-104">Libri telefonici RAS</span><span class="sxs-lookup"><span data-stu-id="81106-104">RAS Phone Books</span></span>

<span data-ttu-id="81106-105">Le rubriche telefoniche forniscono un modo standard per raccogliere e specificare le informazioni necessarie alla gestione connessione di accesso remoto per stabilire una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="81106-105">Phone books provide a standard way to collect and specify the information that the Remote Access Connection Manager needs to establish a remote connection.</span></span> <span data-ttu-id="81106-106">Le rubriche telefoniche associano nomi di voce a informazioni quali numeri di telefono, porte COM e impostazioni del modem.</span><span class="sxs-lookup"><span data-stu-id="81106-106">Phone books associate entry names with information such as phone numbers, COM ports, and modem settings.</span></span> <span data-ttu-id="81106-107">Ogni voce del libro telefonico contiene le informazioni necessarie per stabilire una connessione RAS.</span><span class="sxs-lookup"><span data-stu-id="81106-107">Each phone-book entry contains the information needed to establish a RAS connection.</span></span>

<span data-ttu-id="81106-108">Le rubriche telefoniche sono archiviate in file di testo, ovvero file di testo contenenti i nomi di voce e informazioni associate.</span><span class="sxs-lookup"><span data-stu-id="81106-108">Phone books are stored in phone-book files, which are text files that contain the entry names and associated information.</span></span> <span data-ttu-id="81106-109">RAS crea un file di libro telefonico chiamato RASPHONE. PBK.</span><span class="sxs-lookup"><span data-stu-id="81106-109">RAS creates a phone-book file called RASPHONE.PBK.</span></span> <span data-ttu-id="81106-110">L'utente può utilizzare la finestra di dialogo **connessione remota** principale per creare file personali della Rubrica.</span><span class="sxs-lookup"><span data-stu-id="81106-110">The user can use the main **Dial-Up Networking** dialog box to create personal phone-book files.</span></span> <span data-ttu-id="81106-111">L'API RAS attualmente non fornisce supporto per la creazione di un file di libro telefonico.</span><span class="sxs-lookup"><span data-stu-id="81106-111">The RAS API does not currently provide support for creating a phone-book file.</span></span> <span data-ttu-id="81106-112">Alcune funzioni RAS, ad esempio la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , hanno un parametro che specifica un file della rubrica telefonica.</span><span class="sxs-lookup"><span data-stu-id="81106-112">Some RAS functions, such as the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function, have a parameter that specifies a phone-book file.</span></span> <span data-ttu-id="81106-113">Se il chiamante non specifica un file della rubrica telefonica, la funzione utilizzerà il file predefinito della Rubrica, che è quello selezionato dall'utente nella finestra delle proprietà **Preferenze utente** della finestra di dialogo **connessione remota** .</span><span class="sxs-lookup"><span data-stu-id="81106-113">If the caller does not specify a phone-book file, the function uses the default phone-book file, which is the one selected by the user in the **User Preferences** property sheet of the **Dial-Up Networking** dialog box.</span></span>

<span data-ttu-id="81106-114">Windows NT 4,0 fornisce le funzioni [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) che visualizzano l'interfaccia utente RAS incorporata che consente agli utenti di utilizzare le rubriche telefoniche e le voci della Rubrica.</span><span class="sxs-lookup"><span data-stu-id="81106-114">Windows NT 4.0 provides the [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) and [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) functions that display the built-in RAS user interface that enable users to work with phone books and phone-book entries.</span></span>

<span data-ttu-id="81106-115">**Windows 95:** La rete remota archivia le voci del libro telefonico nel registro di sistema, anziché in un file di libro telefonico.</span><span class="sxs-lookup"><span data-stu-id="81106-115">**Windows 95:** Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.</span></span> <span data-ttu-id="81106-116">Windows 95 non supporta i file o le funzioni personali della rubrica telefonica che visualizzano le finestre di dialogo RAS predefinite.</span><span class="sxs-lookup"><span data-stu-id="81106-116">Windows 95 does not support personal phone-book files or functions that display the built-in RAS dialog boxes.</span></span>

 

 




