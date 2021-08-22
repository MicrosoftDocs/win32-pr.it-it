---
description: Wmiadap è un'applicazione che viene eseguita Windows in grado di aggiornare le informazioni sulle prestazioni nel repository WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a58de2ca5e678cbbb99f803415572be236f2a545ed149b9ad598fb7f9a4664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049839"
---
# <a name="wmiadap"></a>wmiadap

Wmiadap è un'applicazione che viene eseguita Windows in grado di aggiornare le informazioni sulle prestazioni nel repository WMI. In genere, ciò consente agli sviluppatori e agli amministratori IT di creare script che accedono alle informazioni sulle prestazioni, ad esempio la quantità di memoria usata da un'applicazione. L'argomento seguente descrive l'interfaccia della riga di comando che è possibile usare per controllare il modo in cui wmiadap recupera le informazioni.

Wmiadap viene installato con il sistema operativo nella maggior parte dei sistemi, nella directory C: \\ Windows \\ System32 \\ wbem. Se vengono visualizzati messaggi di errore relativi wmiadap.exe, cercare [Supporto tecnico Microsoft](https://support.microsoft.com/). In genere, è consigliabile non wmiadap.exe dal sistema, se non diversamente specificato.

Il trasferimento dei dati dalle librerie delle prestazioni e l'aggiornamento delle classi derivate da [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) vengono estratte dai provider [WmiPerfClass](wmi-providers.md) e [WMIPerfInst.](wmi-providers.md) Il provider WmiPerfClass aggiorna le classi [dei contatori delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI solo quando viene aggiunto un nuovo oggetto prestazioni. È comunque possibile eseguire Wmiadap con **l'opzione /r** per analizzare i driver Windows Driver Model per creare oggetti prestazioni. **L'opzione /f** forza comunque un aggiornamento delle classi WMI dalle librerie delle prestazioni.

Le opzioni seguenti sono disponibili al prompt dei comandi.

**wmiadap** \[ **/f** \] \[ **/r**\]

## <a name="switches"></a>Commutatori

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**/f**
</dt> <dd>

Analizza tutte le librerie delle prestazioni nel sistema e aggiorna le classi derivate da [**\_ Win32 PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Analizza tutti i driver Windows driver nel sistema per creare oggetti prestazioni.

</dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Librerie delle prestazioni e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**Winmgmt**](winmgmt.md)
</dt> </dl>

 

 
