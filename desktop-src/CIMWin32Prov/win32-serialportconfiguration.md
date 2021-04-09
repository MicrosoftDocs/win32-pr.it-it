---
description: La \_ classe WMI SerialPortConfiguration Win32 rappresenta le impostazioni per la trasmissione dei dati su una porta seriale basata su Windows. Sono incluse le configurazioni per stabilire una connessione e il controllo degli errori.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Classe Win32_SerialPortConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965953"
---
# <a name="win32_serialportconfiguration-class"></a><span data-ttu-id="3446a-104">Win32 \_ SerialPortConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="3446a-104">Win32\_SerialPortConfiguration class</span></span>

<span data-ttu-id="3446a-105">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPortConfiguration Win32** rappresenta le impostazioni per la trasmissione dei dati su una porta seriale basata su Windows.</span><span class="sxs-lookup"><span data-stu-id="3446a-105">The **Win32\_SerialPortConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings for data transmission on a Windows-based serial port.</span></span> <span data-ttu-id="3446a-106">Sono incluse le configurazioni per stabilire una connessione e il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="3446a-106">This includes configurations for establishing a connection and error checking.</span></span>

<span data-ttu-id="3446a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3446a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3446a-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3446a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3446a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3446a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a><span data-ttu-id="3446a-110">Members</span><span class="sxs-lookup"><span data-stu-id="3446a-110">Members</span></span>

<span data-ttu-id="3446a-111">La classe **Win32 \_ SerialPortConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3446a-111">The **Win32\_SerialPortConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="3446a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3446a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3446a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3446a-113">Properties</span></span>

<span data-ttu-id="3446a-114">La classe **Win32 \_ SerialPortConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3446a-114">The **Win32\_SerialPortConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3446a-115">**AbortReadWriteOnError**</span><span class="sxs-lookup"><span data-stu-id="3446a-115">**AbortReadWriteOnError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-118">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")</span><span class="sxs-lookup"><span data-stu-id="3446a-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fAbortOnError")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-119">Se **true**, le operazioni di lettura e scrittura vengono interrotte se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="3446a-119">If **TRUE**, read and write operations are terminated if an error occurs.</span></span> <span data-ttu-id="3446a-120">Se **true**, il driver termina tutte le operazioni di lettura e scrittura con uno stato di errore se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="3446a-120">If **TRUE**, the driver terminates all read and write operations with an error status if an error occurs.</span></span> <span data-ttu-id="3446a-121">Il driver non accetterà ulteriori operazioni di comunicazione fino a quando l'errore non verrà riconosciuto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3446a-121">The driver will not accept any further communications operations until the application acknowledges the error.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-122">**BaudRate**</span><span class="sxs-lookup"><span data-stu-id="3446a-122">**BaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-123">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-125">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| baud")</span><span class="sxs-lookup"><span data-stu-id="3446a-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|BaudRate")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-126">Velocità in baud (bit al secondo) con cui il dispositivo di comunicazione funziona.</span><span class="sxs-lookup"><span data-stu-id="3446a-126">Baud (bits per second) rate at which the communications device operates.</span></span>

<span data-ttu-id="3446a-127">Esempio: 9600</span><span class="sxs-lookup"><span data-stu-id="3446a-127">Example: 9600</span></span>

</dd> <dt>

<span data-ttu-id="3446a-128">**BinaryModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="3446a-128">**BinaryModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-129">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-131">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")</span><span class="sxs-lookup"><span data-stu-id="3446a-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-132">Se **true**, i trasferimenti di dati in modalità binaria sono abilitati per la porta seriale.</span><span class="sxs-lookup"><span data-stu-id="3446a-132">If **TRUE**, binary-mode data transfers are enabled for the serial port.</span></span> <span data-ttu-id="3446a-133">I sistemi di computer che eseguono Windows supportano solo i trasferimenti binari tramite porte seriali, quindi questo valore è sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="3446a-133">Computer systems running Windows only allow binary transfers through serial ports, so this value is always **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-134">**BitsPerByte**</span><span class="sxs-lookup"><span data-stu-id="3446a-134">**BitsPerByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-137">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize")</span><span class="sxs-lookup"><span data-stu-id="3446a-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ByteSize")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-138">Numero di bit trasmessi e ricevuti per ogni byte di dati per la porta seriale di Windows.</span><span class="sxs-lookup"><span data-stu-id="3446a-138">Number of bits transmitted and received for each byte of data for the Windows serial port.</span></span> <span data-ttu-id="3446a-139">Il numero può variare con i bit di controllo e di correzione degli errori, ad esempio i bit di parità.</span><span class="sxs-lookup"><span data-stu-id="3446a-139">The number may vary with control and error correction bits, such as parity bits.</span></span>

<span data-ttu-id="3446a-140">Esempio: 8</span><span class="sxs-lookup"><span data-stu-id="3446a-140">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="3446a-141">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="3446a-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3446a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-144">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="3446a-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3446a-145">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="3446a-145">Short textual description of the current object.</span></span>

<span data-ttu-id="3446a-146">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3446a-146">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="3446a-147">**ContinueXMitOnXOff**</span><span class="sxs-lookup"><span data-stu-id="3446a-147">**ContinueXMitOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-150">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")</span><span class="sxs-lookup"><span data-stu-id="3446a-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fTXContinueOnXoff")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-151">Se è **true**, le trasmissioni dei dati continuano quando il buffer di input si trova all'interno di **XOffXMitThreshold** byte di piena e il driver ha trasmesso il valore **XOffChararcter** per interrompere la ricezione dei byte.</span><span class="sxs-lookup"><span data-stu-id="3446a-151">If **TRUE**, data transmissions continue when the input buffer has come within **XOffXMitThreshold** bytes of being full and the driver has transmitted the **XOffChararcter** value to stop receiving bytes.</span></span> <span data-ttu-id="3446a-152">Se **false**, la trasmissione non continua fino a quando il buffer di input non si trova all'interno di **XOnXMitThreshold** byte di essere vuoto e il driver ha trasmesso il valore **XOnCharacter** per riprendere la ricezione.</span><span class="sxs-lookup"><span data-stu-id="3446a-152">If **FALSE**, transmission does not continue until the input buffer is within **XOnXMitThreshold** bytes of being empty and the driver has transmitted the **XOnCharacter** value to resume reception.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-153">**CTSOutflowControl**</span><span class="sxs-lookup"><span data-stu-id="3446a-153">**CTSOutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-154">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-156">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")</span><span class="sxs-lookup"><span data-stu-id="3446a-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxCtsFlow")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-157">Se **true**, il segnale CTS (Clear to Send) viene verificato prima della trasmissione dei dati.</span><span class="sxs-lookup"><span data-stu-id="3446a-157">If **TRUE**, the clear to send (CTS) signal is checked before transmitting data.</span></span> <span data-ttu-id="3446a-158">CTS segnala che entrambi i dispositivi della connessione seriale sono pronti per il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="3446a-158">CTS signals that both devices on the serial connection are ready to transfer data.</span></span> <span data-ttu-id="3446a-159">La trasmissione dei dati viene sospesa fino a quando non viene specificato il segnale CTS.</span><span class="sxs-lookup"><span data-stu-id="3446a-159">Data transmission is suspended until the CTS signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-160">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3446a-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3446a-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3446a-163">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="3446a-163">Textual description of the current object.</span></span>

<span data-ttu-id="3446a-164">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3446a-164">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="3446a-165">**DiscardNULLBytes**</span><span class="sxs-lookup"><span data-stu-id="3446a-165">**DiscardNULLBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-166">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-168">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")</span><span class="sxs-lookup"><span data-stu-id="3446a-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fNull")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-169">Se **true**, i byte **null** (caratteri) vengono eliminati quando vengono ricevuti.</span><span class="sxs-lookup"><span data-stu-id="3446a-169">If **TRUE**, **NULL** bytes (characters) are discarded when they are received.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-170">**DSROutflowControl**</span><span class="sxs-lookup"><span data-stu-id="3446a-170">**DSROutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-171">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-173">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")</span><span class="sxs-lookup"><span data-stu-id="3446a-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxDsrFlow")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-174">Se **true**, il controllo del flusso di dati è abilitato quando è presente una condizione del set di dati (DSR).</span><span class="sxs-lookup"><span data-stu-id="3446a-174">If **TRUE**, data outflow control is enabled when there is a data set ready (DSR) condition.</span></span> <span data-ttu-id="3446a-175">Il DSR segnala che la connessione è stata stabilita dai dispositivi sulla connessione seriale.</span><span class="sxs-lookup"><span data-stu-id="3446a-175">DSR signals that the connection has been established by the devices on the serial connection.</span></span> <span data-ttu-id="3446a-176">La trasmissione dei dati DSR viene sospesa fino a quando non viene specificato il segnale DSR.</span><span class="sxs-lookup"><span data-stu-id="3446a-176">DSR data transmission is suspended until the DSR signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-177">**Riservatezza DSR**</span><span class="sxs-lookup"><span data-stu-id="3446a-177">**DSRSensitivity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-178">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-180">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")</span><span class="sxs-lookup"><span data-stu-id="3446a-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDsrSensitivity")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-181">Se **true**, il driver di comunicazione è sensibile allo stato del segnale DSR.</span><span class="sxs-lookup"><span data-stu-id="3446a-181">If **TRUE**, the communications driver is sensitive to the state of the DSR signal.</span></span> <span data-ttu-id="3446a-182">Il driver ignora tutti i byte ricevuti, a meno che la riga di input del modem DSR non sia alta.</span><span class="sxs-lookup"><span data-stu-id="3446a-182">The driver ignores any bytes received, unless the DSR modem input line is high.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-183">**DTRFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="3446a-183">**DTRFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3446a-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-186">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")</span><span class="sxs-lookup"><span data-stu-id="3446a-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDtrControl")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-187">Uso del controllo di flusso Data Terminal Ready (DTR) dopo che è stata stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="3446a-187">Use of the data terminal ready (DTR) flow control after a connection has been established.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="3446a-188">**Enable** ("Enable")</span><span class="sxs-lookup"><span data-stu-id="3446a-188">**Enable** ("Enable")</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="3446a-189">**Disabilita** ("Disabilita")</span><span class="sxs-lookup"><span data-stu-id="3446a-189">**Disable** ("Disable")</span></span>


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="3446a-190">**Handshake** ("handshake")</span><span class="sxs-lookup"><span data-stu-id="3446a-190">**Handshake** ("Handshake")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3446a-191">**Carattere EOF**</span><span class="sxs-lookup"><span data-stu-id="3446a-191">**EOFCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-192">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-194">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")</span><span class="sxs-lookup"><span data-stu-id="3446a-194">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EofChar")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-195">Valore del carattere utilizzato per segnalare la fine dei dati.</span><span class="sxs-lookup"><span data-stu-id="3446a-195">Value of the character used to signal the end of data.</span></span>

<span data-ttu-id="3446a-196">Esempio: ^ Z</span><span class="sxs-lookup"><span data-stu-id="3446a-196">Example: ^Z</span></span>

</dd> <dt>

<span data-ttu-id="3446a-197">**ErrorReplaceCharacter**</span><span class="sxs-lookup"><span data-stu-id="3446a-197">**ErrorReplaceCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-198">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-200">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")</span><span class="sxs-lookup"><span data-stu-id="3446a-200">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-201">Valore del carattere utilizzato per sostituire i byte ricevuti con un errore di parità.</span><span class="sxs-lookup"><span data-stu-id="3446a-201">Value of the character used to replace bytes received with a parity error.</span></span>

<span data-ttu-id="3446a-202">Esempio: ^ C</span><span class="sxs-lookup"><span data-stu-id="3446a-202">Example: ^C</span></span>

</dd> <dt>

<span data-ttu-id="3446a-203">**ErrorReplacementEnabled**</span><span class="sxs-lookup"><span data-stu-id="3446a-203">**ErrorReplacementEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-204">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-206">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")</span><span class="sxs-lookup"><span data-stu-id="3446a-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-207">Se **true**, i byte ricevuti con errori di parità vengono sostituiti con il valore **ErrorReplaceCharacter** .</span><span class="sxs-lookup"><span data-stu-id="3446a-207">If **TRUE**, bytes received with parity errors are replaced with the **ErrorReplaceCharacter** value.</span></span> <span data-ttu-id="3446a-208">I caratteri con errori di parità vengono sostituiti solo se questa proprietà è **true** e la parità è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3446a-208">Characters with parity errors are only replaced if this property is **TRUE** and the parity is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-209">**EventCharacter**</span><span class="sxs-lookup"><span data-stu-id="3446a-209">**EventCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-210">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-212">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")</span><span class="sxs-lookup"><span data-stu-id="3446a-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EvtChar")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-213">Valore del carattere di controllo utilizzato per segnalare un evento, ad esempio la fine del file.</span><span class="sxs-lookup"><span data-stu-id="3446a-213">Value of the control character that is used to signal an event, such as end of file.</span></span>

<span data-ttu-id="3446a-214">Esempio: ^ e</span><span class="sxs-lookup"><span data-stu-id="3446a-214">Example: ^e</span></span>

</dd> <dt>

<span data-ttu-id="3446a-215">**Della proprietà IsBusy**</span><span class="sxs-lookup"><span data-stu-id="3446a-215">**IsBusy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-216">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-218">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| file functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="3446a-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-219">Se **true**, la porta seriale è occupata.</span><span class="sxs-lookup"><span data-stu-id="3446a-219">If **TRUE**, the serial port is busy.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-220">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3446a-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3446a-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-223">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="3446a-223">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-224">Nome della porta seriale di Windows.</span><span class="sxs-lookup"><span data-stu-id="3446a-224">Name of the Windows serial port.</span></span>

<span data-ttu-id="3446a-225">Esempio: "COM1"</span><span class="sxs-lookup"><span data-stu-id="3446a-225">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="3446a-226">**Parity**</span><span class="sxs-lookup"><span data-stu-id="3446a-226">**Parity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3446a-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-229">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| parità")</span><span class="sxs-lookup"><span data-stu-id="3446a-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|Parity")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-230">Metodo di controllo della parità da usare.</span><span class="sxs-lookup"><span data-stu-id="3446a-230">Method of parity checking to be used.</span></span> <span data-ttu-id="3446a-231">La parità viene utilizzata come una tecnica di controllo degli errori in cui è incluso un bit di parità aggiuntivo con ogni unità di dati.</span><span class="sxs-lookup"><span data-stu-id="3446a-231">Parity is used as an error checking technique where an extra parity bit is included with every unit of data.</span></span> <span data-ttu-id="3446a-232">Il ricevitore può quindi verificare la validità dei dati contando i bit impostati.</span><span class="sxs-lookup"><span data-stu-id="3446a-232">The receiver can then verify the validity of the data by counting the bits that are set.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3446a-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span><span class="sxs-lookup"><span data-stu-id="3446a-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-234">Controllo della parità non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="3446a-234">Parity checking not used.</span></span>

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="3446a-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Dispari ("dispari"** )</span><span class="sxs-lookup"><span data-stu-id="3446a-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Odd** ("Odd")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-236">Imposta il bit di parità in modo che il numero di bit sia dispari.</span><span class="sxs-lookup"><span data-stu-id="3446a-236">Sets the parity bit so that the count of bits set is an odd number.</span></span>

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="3446a-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("even")</span><span class="sxs-lookup"><span data-stu-id="3446a-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-238">Imposta il bit di parità in modo che il numero di bit sia pari.</span><span class="sxs-lookup"><span data-stu-id="3446a-238">Sets the parity bit so that the count of bits set is an even number.</span></span>

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span data-ttu-id="3446a-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Contrassegno** ("contrassegno")</span><span class="sxs-lookup"><span data-stu-id="3446a-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-240">Lascia il bit di parità impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="3446a-240">Leaves the parity bit set to 1.</span></span>

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span data-ttu-id="3446a-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Spazio** ("spazio")</span><span class="sxs-lookup"><span data-stu-id="3446a-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Space** ("Space")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-242">Lascia il bit di parità impostato su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="3446a-242">Leaves the parity bit set to 0 (zero).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3446a-243">**ParityCheckEnabled**</span><span class="sxs-lookup"><span data-stu-id="3446a-243">**ParityCheckEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-244">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3446a-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-246">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")</span><span class="sxs-lookup"><span data-stu-id="3446a-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fParity")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-247">Se **true**, il controllo della parità è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3446a-247">If **TRUE**, parity checking is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-248">**RTSFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="3446a-248">**RTSFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3446a-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3446a-251">Controllo di flusso RTS (request to Send).</span><span class="sxs-lookup"><span data-stu-id="3446a-251">Request to send (RTS) flow control.</span></span> <span data-ttu-id="3446a-252">RTS viene usato per segnalare che i dati sono disponibili per la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="3446a-252">RTS is used to signal that data is available for transmission.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="3446a-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")</span><span class="sxs-lookup"><span data-stu-id="3446a-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-254">La sessione RTS è stata lasciata per la sessione di trasferimento dati.</span><span class="sxs-lookup"><span data-stu-id="3446a-254">RTS is left on for the data transfer session.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="3446a-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** ("Disabilita")</span><span class="sxs-lookup"><span data-stu-id="3446a-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** ("Disable")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-256">RTS viene ignorato dopo la ricezione del primo segnale RTS.</span><span class="sxs-lookup"><span data-stu-id="3446a-256">RTS is ignored after the first RTS signal is received.</span></span>

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="3446a-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("handshake")</span><span class="sxs-lookup"><span data-stu-id="3446a-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-258">RTS è disattivato se il buffer di trasmissione è pieno di tre trimestri e RTS viene attivato quando il buffer è inferiore a una metà.</span><span class="sxs-lookup"><span data-stu-id="3446a-258">RTS is turned off if the transmission buffer is more than three-quarters full, and RTS is turned on when the buffer is less than one-half full.</span></span>

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span data-ttu-id="3446a-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Interruttore** ("interruttore")</span><span class="sxs-lookup"><span data-stu-id="3446a-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Toggle** ("Toggle")</span></span>


</dt> <dd>

<span data-ttu-id="3446a-260">RTS viene attivato se sono presenti dati memorizzati nel buffer per la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="3446a-260">RTS is turned on if there is any data buffered for transmission.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3446a-261">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="3446a-261">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-262">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3446a-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-264">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="3446a-264">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3446a-265">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="3446a-265">Identifier by which the current object is known.</span></span>

<span data-ttu-id="3446a-266">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3446a-266">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="3446a-267">**StopBits**</span><span class="sxs-lookup"><span data-stu-id="3446a-267">**StopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-268">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3446a-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-270">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Stop")</span><span class="sxs-lookup"><span data-stu-id="3446a-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|StopBits")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-271">Numero di bit di interruzione da usare.</span><span class="sxs-lookup"><span data-stu-id="3446a-271">Number of stop bits to be used.</span></span> <span data-ttu-id="3446a-272">I bit stop separano ogni unità di dati in una connessione seriale asincrona.</span><span class="sxs-lookup"><span data-stu-id="3446a-272">Stop bits separate each unit of data on an asynchronous serial connection.</span></span> <span data-ttu-id="3446a-273">Vengono inoltre inviati continuamente quando non sono disponibili dati per la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="3446a-273">They are also sent continuously when no data is available for transmission.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="3446a-274">**1** ("1")</span><span class="sxs-lookup"><span data-stu-id="3446a-274">**1** ("1")</span></span>


</dt> <dd></dd> <dt>

<span id="1.5"></span>

<span data-ttu-id="3446a-275">**1,5** ("1,5")</span><span class="sxs-lookup"><span data-stu-id="3446a-275">**1.5** ("1.5")</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="3446a-276">**2** ("2")</span><span class="sxs-lookup"><span data-stu-id="3446a-276">**2** ("2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3446a-277">**XOffCharacter**</span><span class="sxs-lookup"><span data-stu-id="3446a-277">**XOffCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-278">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-280">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")</span><span class="sxs-lookup"><span data-stu-id="3446a-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffChar")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-281">Valore del carattere XOFF per la trasmissione e la ricezione.</span><span class="sxs-lookup"><span data-stu-id="3446a-281">Value of the XOFF character for both transmission and reception.</span></span> <span data-ttu-id="3446a-282">XOFF è un controllo software per arrestare la trasmissione dei dati (mentre RTS e CTS sono controlli hardware).</span><span class="sxs-lookup"><span data-stu-id="3446a-282">XOFF is a software control to stop the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="3446a-283">XON riprende la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="3446a-283">XON resumes the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-284">**XOffXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="3446a-284">**XOffXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-285">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-287">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")</span><span class="sxs-lookup"><span data-stu-id="3446a-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffLim")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-288">Numero massimo di byte consentiti nel buffer di input prima dell'invio del carattere XOFF.</span><span class="sxs-lookup"><span data-stu-id="3446a-288">Maximum number of bytes allowed in the input buffer before the XOFF character is sent.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-289">**XOnCharacter**</span><span class="sxs-lookup"><span data-stu-id="3446a-289">**XOnCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-290">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-292">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")</span><span class="sxs-lookup"><span data-stu-id="3446a-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonChar")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-293">Valore del carattere XON per la trasmissione e la ricezione.</span><span class="sxs-lookup"><span data-stu-id="3446a-293">Value of the XON character for both transmission and reception.</span></span> <span data-ttu-id="3446a-294">XON è un controllo software per riprendere la trasmissione dei dati (mentre RTS e CTS sono controlli hardware).</span><span class="sxs-lookup"><span data-stu-id="3446a-294">XON is a software control to resume the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="3446a-295">XOFF interrompe la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="3446a-295">XOFF stops the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-296">**XOnXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="3446a-296">**XOnXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-297">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-299">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")</span><span class="sxs-lookup"><span data-stu-id="3446a-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonLim")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-300">Numero minimo di byte consentiti nel buffer di input prima che il carattere XON venga inviato.</span><span class="sxs-lookup"><span data-stu-id="3446a-300">Minimum number of bytes allowed in the input buffer before the XON character is sent.</span></span> <span data-ttu-id="3446a-301">Questa proprietà funziona insieme a **XOffXMitThreshold** per regolare la velocità di trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="3446a-301">This property works in conjunction with **XOffXMitThreshold** to regulate the rate at which data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="3446a-302">**XOnXOffInFlowControl**</span><span class="sxs-lookup"><span data-stu-id="3446a-302">**XOnXOffInFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-303">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-303">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-305">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")</span><span class="sxs-lookup"><span data-stu-id="3446a-305">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fInX")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-306">Se **true**, il controllo di flusso XON/XOFF viene usato durante la ricezione.</span><span class="sxs-lookup"><span data-stu-id="3446a-306">If **TRUE**, XON/XOFF flow control is used during reception.</span></span> <span data-ttu-id="3446a-307">Se **true**, il valore **XOffCharacter** viene inviato quando il buffer di input si trova all'interno di **XOffXMitThreshold** byte di riempimento e il valore di **XOnCharacter** viene inviato quando il buffer di input rientra in **XOnXMitThreshold** byte di essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="3446a-307">If **TRUE**, the **XOffCharacter** value is sent when the input buffer comes within **XOffXMitThreshold** bytes of being full, and the **XOnCharacter** value is sent when the input buffer comes within **XOnXMitThreshold** bytes of being empty.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="3446a-308"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="3446a-308"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="3446a-309">FALSE</span><span class="sxs-lookup"><span data-stu-id="3446a-309">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="3446a-310"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="3446a-310"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="3446a-311">true</span><span class="sxs-lookup"><span data-stu-id="3446a-311">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3446a-312">**XOnXOffOutFlowControl**</span><span class="sxs-lookup"><span data-stu-id="3446a-312">**XOnXOffOutFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3446a-313">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3446a-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3446a-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3446a-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3446a-315">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")</span><span class="sxs-lookup"><span data-stu-id="3446a-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutX")</span></span>
</dt> </dl>

<span data-ttu-id="3446a-316">**XOnXOffOutFlowControl** specifica se il controllo di flusso XON o XOFF viene usato durante la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="3446a-316">The **XOnXOffOutFlowControl** specifies whether XON or XOFF flow control is used during transmission.</span></span> <span data-ttu-id="3446a-317">Se è **true**, la trasmissione si interrompe quando viene ricevuto il valore **XOffCharacter** e viene riavviato quando viene ricevuto il valore **XOnCharacter** .</span><span class="sxs-lookup"><span data-stu-id="3446a-317">If **TRUE**, transmission stops when the **XOffCharacter** value is received and starts again when the **XOnCharacter** value is received.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3446a-318">Commenti</span><span class="sxs-lookup"><span data-stu-id="3446a-318">Remarks</span></span>

<span data-ttu-id="3446a-319">La classe **Win32 \_ SerialPortConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="3446a-319">The **Win32\_SerialPortConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3446a-320">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3446a-320">Requirements</span></span>



| <span data-ttu-id="3446a-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="3446a-321">Requirement</span></span> | <span data-ttu-id="3446a-322">Valore</span><span class="sxs-lookup"><span data-stu-id="3446a-322">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3446a-323">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3446a-323">Minimum supported client</span></span><br/> | <span data-ttu-id="3446a-324">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3446a-324">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3446a-325">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3446a-325">Minimum supported server</span></span><br/> | <span data-ttu-id="3446a-326">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3446a-326">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3446a-327">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3446a-327">Namespace</span></span><br/>                | <span data-ttu-id="3446a-328">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3446a-328">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3446a-329">MOF</span><span class="sxs-lookup"><span data-stu-id="3446a-329">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3446a-330"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3446a-330"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3446a-331">DLL</span><span class="sxs-lookup"><span data-stu-id="3446a-331">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3446a-332"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3446a-332"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3446a-333">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3446a-333">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3446a-334">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="3446a-334">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="3446a-335">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="3446a-335">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
