---
description: Eseguire il backup dei volumi mentre le applicazioni in un sistema continuano a scrivere nei volumi. Ridurre al minimo i tempi di inattività dell'applicazione creando rapidamente uno snapshot (copia shadow) di un volume che duplica tutti i dati. Eseguire il backup multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2159d39f407f7ae5dbde454ab6cf3562307d892c
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443082"
---
# <a name="volume-shadow-copy-service"></a>Servizio Copia Shadow del volume

## <a name="purpose"></a>Scopo

Il Servizio Copia Shadow del volume (VSS) è un set di interfacce COM che implementa un framework per consentire l'esecuzione di backup dei volumi mentre le applicazioni in un sistema continuano a scrivere nei volumi.

Per un'introduzione a VSS per gli amministratori di sistema, [Servizio Copia Shadow del volume](/windows-server/storage/file-server/volume-shadow-copy-service) nella libreria TechNet.

## <a name="run-time-requirements"></a>Requisiti di runtime

VSS è supportato in Microsoft Windows XP e versioni successive. Per informazioni sui requisiti di run-time per un particolare elemento di programmazione, vedere la sezione Requisiti della documentazione relativa a tale elemento.

Tutte le applicazioni VSS a 32 bit (richiedenti, provider e writer) devono essere eseguite come applicazioni native a 32 bit o a 64 bit. L'esecuzione in WOW64 non è supportata. Per altre informazioni, vedere [Configurazioni e restrizioni supportate.](usage-conventions.md)

**Windows Server 2003 e Windows XP:** L'esecuzione di richiedenti VSS a 32 bit in WOW64 è supportata, ma non per i backup dello stato del sistema. L'esecuzione di provider e writer VSS a 32 bit in WOW64 non è supportata. Il supporto per l'esecuzione di richiedenti a 32 bit in WOW64 è stato rimosso in Windows Vista e nelle versioni successive.

> [!Note]  
> Una copia shadow creata in Windows Server 2003 R2 o Windows Server 2003 non può essere usata in un computer che esegue Windows Server 2008 R2 o Windows Server 2008. Una copia shadow creata in Windows Server 2008 R2 o Windows Server 2008 non può essere usata in un computer che esegue Windows Server 2003. Tuttavia, una copia shadow creata in Windows Server 2008 può essere utilizzata in un computer che esegue Windows Server 2008 R2 e viceversa.

 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                          | Descrizione                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Panoramica](volume-shadow-copy-service-overview.md)<br/> | Descrive il modello a oggetti vss, le strategie di backup e ripristino e come creare provider, richiedenti e writer vss.<br/> |
| [Riferimento](volume-shadow-copy-reference.md)<br/>       | Descrive le classi, i tipi di dati, le enumerazioni, le funzioni, le interfacce e le strutture vss.<br/>                                  |



 

## <a name="additional-resources"></a>Risorse aggiuntive



|   Risorsa                                 |   Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista e versioni successive            | VSS è disponibile in Microsoft Windows Software Development Kit (Windows SDK) (SDK). È possibile installare l'SDK per Windows 7 e Windows Server 2008 R2 [dall'Area download Windows.](https://www.microsoft.com/download/details.aspx?id=8279) È anche possibile scaricare la [versione ISO dell'SDK](https://www.microsoft.com/download/details.aspx?id=8442) dall'Area download Windows. Le versioni precedenti dell'SDK possono essere scaricate dalla [Windows SDK download.](https://msdn.microsoft.com/windows/bb980924.aspx) |
| Windows Server 2003 e Windows XP | VSS è disponibile in Servizio Copia Shadow del volume 7.2 SDK, che è possibile scaricare [dall'Area download Windows.](https://www.microsoft.com/download/details.aspx?id=23490) Si noti che i file vssapi.lib a 64 bit nelle directory nella directory Obj di Win2003 possono essere usati per le versioni a \\ 64 bit di Windows Server 2003 e Windows XP.                                                                                                                                                                 |



 

 

 
