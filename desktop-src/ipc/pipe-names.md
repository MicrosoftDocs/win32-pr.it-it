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
# <a name="pipe-names"></a>Nomi pipe

Ogni named pipe dispone di un nome univoco che lo distingue dalle altre named pipe nell'elenco di oggetti denominati del sistema. Un server pipe specifica un nome per la pipe quando chiama la funzione [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) per creare una o più istanze di una named pipe. I client pipe specificano il nome della pipe quando chiamano la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) per connettersi a un'istanza del named pipe.

Utilizzare il formato seguente quando si specifica il nome di una pipe nella funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) :

\\\\*Nomeserver* \\ \\ pipeName pipe

dove *nomeserver* è il nome di un computer remoto o un punto, per specificare il computer locale. La stringa del nome pipe specificata da *pipeName* può includere qualsiasi carattere diverso da una barra rovesciata, inclusi i numeri e i caratteri speciali. La lunghezza totale della stringa del nome della pipe può essere di 256 caratteri. I nomi delle pipe non fanno distinzione tra maiuscole e minuscole.

Il server pipe non è in grado di creare una pipe in un altro computer, quindi [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) deve usare un punto per il nome del server, come illustrato nell'esempio seguente.

\\\\.\\ \\ pipeName pipe

Un server pipe può fornire il nome della pipe ai client pipe, in modo da potersi connettere alla pipe. Il client pipe individua il nome della pipe da un'origine persistente, ad esempio una voce del registro di sistema, un file o un'altra applicazione. In caso contrario, è necessario che i client conoscano il nome della pipe in fase di compilazione.

 

 
