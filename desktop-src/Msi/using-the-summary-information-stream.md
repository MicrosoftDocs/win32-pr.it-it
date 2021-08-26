---
description: Questa sezione descrive le funzioni nell'API Windows Installer possono chiamare le proprietà del flusso di informazioni di riepilogo. Per altre informazioni sul flusso di informazioni di riepilogo e sul funzionamento con i database, vedere Informazioni sul flusso di informazioni di riepilogo.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Uso del flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a90d6be9586ab6adc469f14fea71dc1325cb19107bd8ddc634a3d0b4463c490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996041"
---
# <a name="using-the-summary-information-stream"></a>Uso del flusso di informazioni di riepilogo

Questa sezione descrive le funzioni nell'API Windows Installer possono chiamare le proprietà del flusso di informazioni di riepilogo. Per altre informazioni sul flusso di informazioni di riepilogo e sul funzionamento con i database, vedere [Informazioni sul flusso di informazioni di riepilogo](about-the-summary-information-stream.md).

-   È importante ricordare che il programma di installazione contiene diversi tipi di database e alcune proprietà del flusso di informazioni di riepilogo hanno significati diversi con database diversi. Per altre informazioni, vedere [Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md).
-   Quando un database viene aperto come output di un altro database, il flusso di informazioni di riepilogo del database di output è in realtà un mirror di sola lettura del database originale e pertanto non può essere modificato. Inoltre, non verrà salvato in modo permanente con il database. Per creare o modificare le informazioni di riepilogo per il database di output, è necessario chiuderlo e riaperrlo.

La procedura seguente descrive come usare le funzioni del flusso di informazioni di riepilogo:

**Per usare le proprietà del flusso di informazioni di riepilogo**

1.  Ottenere un handle per il database contenente il flusso di informazioni di riepilogo chiamando la [**funzione MsiGetSummaryInformation.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)
2.  Chiamare la [**funzione MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) per ottenere il numero di proprietà esistenti.
3.  Chiamare la [**funzione MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) per visualizzare una singola proprietà di informazioni di riepilogo.
4.  Chiamare la [**funzione MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) per impostare una singola proprietà
5.  Chiamare la [**funzione MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) per salvare la proprietà delle informazioni di riepilogo.
6.  Chiamare la [**funzione MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) per creare le informazioni di riepilogo per una trasformazione esistente.

[Orca.exe](orca-exe.md) e [Msiinfo.exe](msiinfo-exe.md) sono strumenti che possono essere usati per modificare o visualizzare il flusso di informazioni di riepilogo di un database. Questi strumenti sono disponibili solo nei componenti di [Windows SDK per Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

È anche possibile accedere al flusso di informazioni di riepilogo usando i metodi e le proprietà seguenti dell'Windows di automazione [del programma di installazione.](automation-interface.md)

-   [**SummaryInfo.Property**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo.PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo.Persist**](summaryinfo-persist.md)
-   [**Installer.SummaryInformation**](installer-summaryinformation.md)
-   [**Database.SummaryInformation**](database-summaryinformation.md)
-   [**Database.CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md)

Il file VBScript WiSumInf.vbs è disponibile in componenti dell'SDK Windows per [Windows programma di installazione.](platform-sdk-components-for-windows-installer-developers.md) Questo script di esempio può essere usato per gestire il flusso di informazioni di riepilogo di un pacchetto Windows installer. Per altre informazioni sui WiSumInf.vbs, vedere [Gestire le informazioni di riepilogo](manage-summary-information.md).

 

 



