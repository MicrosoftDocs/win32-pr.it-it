---
description: Windows Installer viene eseguito come servizio nei computer che utilizzano Windows a 32 bit o a 64 bit.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Informazioni Windows Installer sui sistemi operativi a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "104234369"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a>Informazioni Windows Installer sui sistemi operativi a 64 bit

Windows Installer viene eseguito come servizio nei computer che utilizzano Windows a 32 bit o a 64 bit. Le versioni del programma di installazione precedenti alla versione 2,0 possono installare e gestire i pacchetti Windows Installer a 32 bit solo nei sistemi operativi a 32 bit. Si noti che non è possibile pubblicizzare o installare un'applicazione a 64 bit in un sistema operativo a 32 bit.

È necessario specificare un pacchetto di Windows Installer come pacchetto a 32 bit o a 64 bit. non può essere specificato come neutro. In un computer che utilizza un sistema operativo a 64 bit, il servizio Windows Installer è ospitato in un processo a 64 bit che consente di installare sia i pacchetti 32 bit che quelli a 64 bit. Windows Installer installa tre tipi di pacchetti di Windows Installer in un computer in cui è in esecuzione un sistema operativo a 64 bit:

-   Pacchetti a 32 bit che contengono solo componenti a 32 bit.
-   Pacchetti a 64 bit contenenti alcuni componenti a 32 bit.
-   Pacchetti a 64 bit contenenti solo componenti a 64 bit.

Le sezioni seguenti descrivono i due tipi di pacchetti di Windows Installer e le nuove proprietà del programma di installazione fornite da Windows Installer per i pacchetti a 64 bit.

[Pacchetti Windows Installer a 32 bit](32-bit-windows-installer-packages.md)

[Pacchetti Windows Installer a 64 bit](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di pacchetti di Windows Installer a 64 bit](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



