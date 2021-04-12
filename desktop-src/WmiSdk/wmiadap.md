---
description: Wmiadap è un'applicazione eseguita in Windows in grado di aggiornare le informazioni sulle prestazioni nel repository WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233976"
---
# <a name="wmiadap"></a>wmiadap

Wmiadap è un'applicazione eseguita in Windows in grado di aggiornare le informazioni sulle prestazioni nel repository WMI. In genere, questo consente agli sviluppatori e agli amministratori IT di creare script che accedono alle informazioni sulle prestazioni, ad esempio la quantità di memoria usata da un'applicazione. Nell'argomento seguente viene descritta l'interfaccia della riga di comando che è possibile utilizzare per controllare il modo in cui wmiadap recupera le informazioni.

Wmiadap viene installato con il sistema operativo nella maggior parte dei sistemi, nella directory C: \\ Windows \\ system32 \\ WBEM. Se vengono visualizzati messaggi di errore relativi wmiadap.exe, cercare [supporto tecnico Microsoft](https://support.microsoft.com/). In genere, non è consigliabile eliminare wmiadap.exe dal sistema, se non diversamente indicato.

Il trasferimento dei dati dalle librerie di prestazioni e l'aggiornamento delle classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) vengono eseguiti dai provider [wmiperfclass](wmi-providers.md) e [wmiperfinst](wmi-providers.md) . Il provider WmiPerfClass Aggiorna [le classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI solo quando viene aggiunto un nuovo oggetto prestazioni. È comunque possibile eseguire wmiadap con l'opzione **/r** per analizzare i driver Windows Driver Model per creare gli oggetti prestazioni. L'opzione **/f** forza ancora un aggiornamento delle classi WMI dalle librerie delle prestazioni.

Al prompt dei comandi sono disponibili le opzioni seguenti.

**wmiadap** \[  \] /f \[ **/r**\]

## <a name="switches"></a>Commutatori

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**/f**
</dt> <dd>

Analizza tutte le librerie di prestazioni nel sistema e aggiorna le classi derivate da [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Analizza tutti i driver Windows Driver Model nel sistema per creare gli oggetti prestazioni.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Librerie di prestazioni e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**winmgmt**](winmgmt.md)
</dt> </dl>

 

 
