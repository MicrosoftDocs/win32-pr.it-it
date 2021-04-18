---
description: Ogni named pipe dispone di un nome univoco che lo distingue dalle altre named pipe nell'elenco dei sistemi degli oggetti denominati. Un server pipe specifica un nome per la pipe quando chiama la funzione CreateNamedPipe per creare una o più istanze di una named pipe.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Nomi pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317314"
---
# <a name="pipe-names"></a><span data-ttu-id="30a76-104">Nomi pipe</span><span class="sxs-lookup"><span data-stu-id="30a76-104">Pipe Names</span></span>

<span data-ttu-id="30a76-105">Ogni named pipe dispone di un nome univoco che lo distingue dalle altre named pipe nell'elenco di oggetti denominati del sistema.</span><span class="sxs-lookup"><span data-stu-id="30a76-105">Each named pipe has a unique name that distinguishes it from other named pipes in the system's list of named objects.</span></span> <span data-ttu-id="30a76-106">Un server pipe specifica un nome per la pipe quando chiama la funzione [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) per creare una o più istanze di una named pipe.</span><span class="sxs-lookup"><span data-stu-id="30a76-106">A pipe server specifies a name for the pipe when it calls the [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) function to create one or more instances of a named pipe.</span></span> <span data-ttu-id="30a76-107">I client pipe specificano il nome della pipe quando chiamano la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) per connettersi a un'istanza del named pipe.</span><span class="sxs-lookup"><span data-stu-id="30a76-107">Pipe clients specify the pipe name when they call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function to connect to an instance of the named pipe.</span></span>

<span data-ttu-id="30a76-108">Utilizzare il formato seguente quando si specifica il nome di una pipe nella funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) :</span><span class="sxs-lookup"><span data-stu-id="30a76-108">Use the following form when specifying the name of a pipe in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea), or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function:</span></span>

<span data-ttu-id="30a76-109">\\\\*Nomeserver* \\ \\ pipeName pipe</span><span class="sxs-lookup"><span data-stu-id="30a76-109">\\\\*ServerName*\\pipe\\*PipeName*</span></span>

<span data-ttu-id="30a76-110">dove *nomeserver* è il nome di un computer remoto o un punto, per specificare il computer locale.</span><span class="sxs-lookup"><span data-stu-id="30a76-110">where *ServerName* is either the name of a remote computer or a period, to specify the local computer.</span></span> <span data-ttu-id="30a76-111">La stringa del nome pipe specificata da *pipeName* può includere qualsiasi carattere diverso da una barra rovesciata, inclusi i numeri e i caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="30a76-111">The pipe name string specified by *PipeName* can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="30a76-112">La lunghezza totale della stringa del nome della pipe può essere di 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="30a76-112">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="30a76-113">I nomi delle pipe non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="30a76-113">Pipe names are not case-sensitive.</span></span>

<span data-ttu-id="30a76-114">Il server pipe non è in grado di creare una pipe in un altro computer, quindi [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) deve usare un punto per il nome del server, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="30a76-114">The pipe server cannot create a pipe on another computer, so [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) must use a period for the server name, as shown in the following example.</span></span>

<span data-ttu-id="30a76-115">\\\\.\\ \\ pipeName pipe</span><span class="sxs-lookup"><span data-stu-id="30a76-115">\\\\.\\pipe\\*PipeName*</span></span>

<span data-ttu-id="30a76-116">Un server pipe può fornire il nome della pipe ai client pipe, in modo da potersi connettere alla pipe.</span><span class="sxs-lookup"><span data-stu-id="30a76-116">A pipe server can provide the pipe name to its pipe clients, so they can connect to the pipe.</span></span> <span data-ttu-id="30a76-117">Il client pipe individua il nome della pipe da un'origine persistente, ad esempio una voce del registro di sistema, un file o un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="30a76-117">The pipe client discovers the pipe name from some persistent source, such as a registry entry, a file, or another application.</span></span> <span data-ttu-id="30a76-118">In caso contrario, è necessario che i client conoscano il nome della pipe in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="30a76-118">Otherwise, the clients must know the pipe name at compile time.</span></span>

 

 
