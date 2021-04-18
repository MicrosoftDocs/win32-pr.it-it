---
description: Questo evento di controllo esegue un file specificato. Se il file non esiste o se l'evento ha esito negativo, Windows Installer registra l'errore nel log dettagliato senza visualizzare una finestra di dialogo contenente un messaggio di errore.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: ControlEvent MsiLaunchApp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309470"
---
# <a name="msilaunchapp-controlevent"></a><span data-ttu-id="31be6-104">ControlEvent MsiLaunchApp</span><span class="sxs-lookup"><span data-stu-id="31be6-104">MsiLaunchApp ControlEvent</span></span>

<span data-ttu-id="31be6-105">Questo evento di controllo esegue un file specificato.</span><span class="sxs-lookup"><span data-stu-id="31be6-105">This control event runs a specified file.</span></span> <span data-ttu-id="31be6-106">Se il file non esiste o se l'evento ha esito negativo, Windows Installer registra l'errore nel log dettagliato senza visualizzare una finestra di dialogo contenente un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="31be6-106">If the file does not exist, or if the event fails, Windows Installer logs the error in the verbose log without displaying a dialog box containing an error message.</span></span>

<span data-ttu-id="31be6-107">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="31be6-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="31be6-108">Questo ControlEvent è disponibile a partire da Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="31be6-108">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

## <a name="published-by"></a><span data-ttu-id="31be6-109">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="31be6-109">Published By</span></span>

<span data-ttu-id="31be6-110">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="31be6-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="31be6-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="31be6-111">Argument</span></span>

<span data-ttu-id="31be6-112">I campi del valore dell'argomento sono delimitati da spazi.</span><span class="sxs-lookup"><span data-stu-id="31be6-112">The fields of the argument value are delimited by spaces.</span></span> <span data-ttu-id="31be6-113">Il primo campo contiene un valore stringa che specifica il file da eseguire.</span><span class="sxs-lookup"><span data-stu-id="31be6-113">The first field contains a string value that specifies the file that is to be run.</span></span> <span data-ttu-id="31be6-114">Usare un valore stringa di \[ \# *FileKey* \] per identificare il file e sostituire *FileKey* con l'identificatore del file visualizzato nella colonna file della tabella [file](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="31be6-114">Use a string value of \[\#*filekey*\] to identify the file and replace *filekey* with the file's identifier appearing in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="31be6-115">Tutti i campi rimanenti dell'argomento possono contenere parametri usati dal file in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="31be6-115">Any remaining fields of the argument can contain parameters being used by the file being run.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="31be6-116">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="31be6-116">Action on Subscribers</span></span>

<span data-ttu-id="31be6-117">Questo ControlEvent non esegue alcuna azione nei Sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="31be6-117">This ControlEvent performs no actions on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="31be6-118">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="31be6-118">Typical Use</span></span>

<span data-ttu-id="31be6-119">Per consentire a un utente di scegliere di eseguire un file al termine di un'installazione.</span><span class="sxs-lookup"><span data-stu-id="31be6-119">To enable a user to choose to run a file at the end of an installation.</span></span> <span data-ttu-id="31be6-120">Questo evento può essere condizionato da una proprietà impostata da un controllo [CheckBox](checkbox-control.md) visualizzato nella finestra di dialogo finale dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="31be6-120">This event can be conditioned on a property set by a [CheckBox](checkbox-control.md) control displayed on the final dialog box of the installation.</span></span> <span data-ttu-id="31be6-121">Il controllo CheckBox non deve essere visualizzato durante la rimozione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="31be6-121">The CheckBox control should not be displayed during the removal of the package.</span></span>

 

 



