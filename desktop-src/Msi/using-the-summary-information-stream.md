---
description: Questa sezione descrive quali funzioni nell'API Windows Installer possono chiamare le proprietà del flusso di informazioni di riepilogo. Per ulteriori informazioni sul flusso di informazioni di riepilogo e sul relativo funzionamento con i database, vedere informazioni sul flusso di informazioni di riepilogo.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Uso del flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de3ece9ad336b1a88d343b859fd3881b23246c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967550"
---
# <a name="using-the-summary-information-stream"></a>Uso del flusso di informazioni di riepilogo

Questa sezione descrive quali funzioni nell'API Windows Installer possono chiamare le proprietà del flusso di informazioni di riepilogo. Per ulteriori informazioni sul flusso di informazioni di riepilogo e sul relativo funzionamento con i database, vedere informazioni sul [flusso di informazioni di riepilogo](about-the-summary-information-stream.md).

-   È importante ricordare che il programma di installazione contiene tipi diversi di database e che alcune proprietà del flusso di informazioni di riepilogo hanno significati diversi con database diversi. Per altre informazioni, vedere [descrizioni delle proprietà di riepilogo](summary-property-descriptions.md).
-   Quando un database viene aperto come output di un altro database, il flusso di informazioni di riepilogo del database di output è effettivamente un mirror di sola lettura del database originale e pertanto non può essere modificato. Inoltre, non verrà reso permanente con il database. Per creare o modificare le informazioni di riepilogo per il database di output, è necessario chiuderlo e riaprirlo.

Nei passaggi seguenti viene descritto come utilizzare le funzioni del flusso di informazioni di riepilogo:

**Per utilizzare le proprietà del flusso di informazioni di riepilogo**

1.  Ottenere un handle per il database contenente il flusso di informazioni di riepilogo chiamando la funzione [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) .
2.  Chiamare la funzione [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) per ottenere il numero di proprietà esistenti.
3.  Chiamare la funzione [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) per visualizzare una singola proprietà di informazioni di riepilogo.
4.  Chiamare la funzione [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) per impostare una singola proprietà
5.  Chiamare la funzione [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) per salvare la proprietà informazioni di riepilogo.
6.  Chiamare la funzione [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) per creare le informazioni di riepilogo per una trasformazione esistente.

[Orca.exe](orca-exe.md) e [Msiinfo.exe](msiinfo-exe.md) sono strumenti che possono essere utilizzati per modificare o visualizzare il flusso di informazioni di riepilogo di un database. Questi strumenti sono disponibili solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

È possibile accedere al flusso di informazioni di riepilogo anche usando i metodi e le proprietà seguenti dell' [interfaccia di automazione](automation-interface.md)del Windows Installer.

-   [**SummaryInfo. Property**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo. PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo. perseverare**](summaryinfo-persist.md)
-   [**Programma di installazione. SummaryInformation**](installer-summaryinformation.md)
-   [**Database. SummaryInformation**](database-summaryinformation.md)
-   [**Database. CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md)

Il file VBScript WiSumInf.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio può essere utilizzato per gestire il flusso di informazioni di riepilogo di un pacchetto di Windows Installer. Per ulteriori informazioni su WiSumInf.vbs, vedere [gestione delle informazioni di riepilogo](manage-summary-information.md).

 

 



