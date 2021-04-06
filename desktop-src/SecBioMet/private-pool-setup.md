---
title: Impostazione del pool privato
description: Contiene il progetto della console di installazione.
ms.assetid: 0B00690C-9B13-4D8B-8AB6-F8BD2E35858C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a661e65610e6cefb03ee9d47f70d7dc8d6d92a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045144"
---
# <a name="private-pool-setup"></a>Impostazione del pool privato

Le sezioni seguenti contengono il codice necessario per configurare un pool di sensori privati.

-   [Targetver. h](#targetverh)
-   [Stdafx. h](#stdafxh)
-   [PrivatePoolCommonDefs. h](#privatepoolcommondefsh)
-   [PrivatePoolSetup. cpp](#privatepoolsetupcpp)

## <a name="targetverh"></a>Targetver. h

Questo esempio è stato creato per i sistemi operativi Windows 7 e versioni successive.


```C++
#pragma once
#ifndef _WIN32_WINNT            
#define _WIN32_WINNT NTDDI_WIN7 
#endif
```



## <a name="stdafxh"></a>stdafx.h


```C++
// stdafx.h : include file for standard system include files,
// or project specific include files that are used frequently but
// are changed infrequently
//
#pragma once

#include "targetver.h"

// Use secure (template) versions of nonsecure 
// CRT text routines
#define _CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES     1

#include <stdio.h>
#include <tchar.h>

#include <windows.h>
#include <winbio.h>

#include "BioHelper.h"

#ifndef ARGUMENT_PRESENT
#define ARGUMENT_PRESENT(x) (((x) != NULL))
#endif
```



## <a name="privatepoolcommondefsh"></a>PrivatePoolCommonDefs. h

Includere l'intestazione seguente. Si noti che è necessario generare un ID database univoco. Non usare il GUID specificato in un'applicazione rilasciata.


```C++
/******************************************************************************
THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED
TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
PARTICULAR PURPOSE.

Copyright (C) Microsoft.  All rights reserved.

This source code is only intended as a supplement to Microsoft Development
Tools and/or WinHelp documentation.  See these sources for detailed information
regarding the Microsoft samples programs.
******************************************************************************/

#pragma once

// Common defintions used by all three programs

// NOTE: DO *NOT* USE THIS GUID VALUE FOR A REAL
// APPLICATION. GENERATE YOUR OWN UNIQUE GUID AND
// REPLACE THE FOLLOWING DEFINITION!
//
// {5086745D-B3F9-4da7-859E-9CC4331CE47C}
static const GUID PRIVATE_POOL_DATABASE_ID = 
{ 0x5086745d, 0xb3f9, 0x4da7, { 0x85, 0x9e, 0x9c, 0xc4, 0x33, 0x1c, 0xe4, 0x7c } };
```



## <a name="privatepoolsetupcpp"></a>PrivatePoolSetup. cpp

Nel codice sorgente seguente viene visualizzato il punto di ingresso per un'applicazione del pool di sensori privati.


```C++
/******************************************************************************
THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED
TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
PARTICULAR PURPOSE.

Copyright (C) Microsoft.  All rights reserved.

This source code is only intended as a supplement to Microsoft Development
Tools and/or WinHelp documentation.  See these sources for detailed information
regarding the Microsoft samples programs.
******************************************************************************/

// PrivatePoolSetup.cpp : Defines the entry point for the console application.
//

#include "stdafx.h"
#include "PrivatePoolCommonDefs.h"   // From Private Pool Setup
#include "Strsafe.h"                 // For StringCbGets()

#include <vector>

// Forward declarations of local functions.
//
static void onInstall();
static void onUninstall();
static void onAdd();
static void onRemove();

static bool selectSensorMenu(
    __in LPCTSTR Prompt,
    __in WINBIO_UNIT_SCHEMA *UnitArray,
    __in SIZE_T UnitCount,
    __out SIZE_T *SelectedUnit
    );

static bool isDatabaseInstalled(
    __in WINBIO_UUID *DatabaseId,
    __out WINBIO_UUID *DataFormat
    );

//-----------------------------------------------------------------------------

int _tmain(int argc, _TCHAR* argv[])
{
    HRESULT hr = S_OK;
    bool databaseInstalled = false;
    WINBIO_UUID dataFormat = {};

    _tprintf( _T("\nWinBio Private Pool Setup\n\n"));

    if (argc < 2)
    {
        _tprintf(_T("Usage: %s -install | -uninstall | -add | -remove\n"), argv[0]);
        _tprintf(
            _T("\n")
            _T("  -install      define private template database\n")
            _T("  -uninstall    detach all sensors from private database and delete database\n")
            _T("  -add          attach (one) specific sensor to private database\n")
            _T("  -remove       detach (one) specific sensor from private database\n")
            _T("\n")
            );
    }
    else
    {
        if (_tcsicmp( argv[1], _T("-install")) == 0)
        {
            onInstall();
        }
        else if (_tcsicmp( argv[1], _T("-uninstall")) == 0)
        {
            onUninstall();
        }
        else if (_tcsicmp( argv[1], _T("-add")) == 0)
        {
            onAdd();
        }
        else if (_tcsicmp( argv[1], _T("-remove")) == 0)
        {
            onRemove();
        }
        else
        {
            _tprintf(_T("*** Error - Unknown command option: %s\n"), argv[1]);
        }
    }

    return 0;
}

//-----------------------------------------------------------------------------

static void onInstall()
{
    WINBIO_UUID databaseId = PRIVATE_POOL_DATABASE_ID;
    WINBIO_UUID dataFormat = {};

    if (isDatabaseInstalled( &databaseId, &dataFormat))
    {
        _tprintf(_T("*** Error - private database already installed.\n"));
        return;
    }

    WINBIO_UNIT_SCHEMA *unitArray = NULL;
    SIZE_T unitCount = 0;
    HRESULT hr = WinBioEnumBiometricUnits( 
                    WINBIO_TYPE_FINGERPRINT, 
                    &unitArray, 
                    &unitCount 
                    );
    if (SUCCEEDED(hr))
    {
        SIZE_T selectedUnit = 0;
        if (selectSensorMenu( 
                _T("Make templates compatible with the selected sensor"), 
                unitArray, 
                unitCount, 
                &selectedUnit
                ))
        {
            BioHelper::POOL_CONFIGURATION derivedConfig = {};
            hr = BioHelper::CreateCompatibleConfiguration( 
                    &unitArray[selectedUnit], 
                    &derivedConfig 
                    );
            if (SUCCEEDED(hr))
            {
                WINBIO_STORAGE_SCHEMA storageSchema = {};
                storageSchema.DatabaseId = PRIVATE_POOL_DATABASE_ID;
                storageSchema.DataFormat = derivedConfig.DataFormat;
                storageSchema.Attributes = derivedConfig.DatabaseAttributes;
                hr = BioHelper::RegisterDatabase( &storageSchema );
            }
        }
        else
        {
            hr = E_INVALIDARG;
        }
        WinBioFree( unitArray );
        unitArray = NULL;
        unitCount = 0;
    }
    if (SUCCEEDED(hr))
    {
        _tprintf(_T("- Private database installed.\n"));
    }
    else
    {
        LPTSTR errorMessage = BioHelper::ConvertErrorCodeToString( hr );
        _tprintf(_T("*** Error - %s\n"), errorMessage );
        LocalFree(errorMessage);
        errorMessage = NULL;
    }
}

//-----------------------------------------------------------------------------

static void onUninstall()
{
    WINBIO_UUID databaseId = PRIVATE_POOL_DATABASE_ID;
    WINBIO_UUID dataFormat = {};

    if (!isDatabaseInstalled( &databaseId, &dataFormat))
    {
        _tprintf(_T("*** Error - private database not installed.\n"));
        return;
    }

    // Remove biometric unit registrations.
    WINBIO_UNIT_SCHEMA *unitArray = NULL;
    SIZE_T unitCount = 0;

    HRESULT hr = WinBioEnumBiometricUnits( 
                    WINBIO_TYPE_FINGERPRINT, 
                    &unitArray, 
                    &unitCount 
                    );
    if (SUCCEEDED(hr))
    {
        for (SIZE_T i = 0; i < unitCount; ++i)
        {
            bool configRemoved = false;
            hr = BioHelper::UnregisterPrivateConfiguration( 
                                &unitArray[i], 
                                &databaseId, 
                                &configRemoved 
                                );
            if (FAILED(hr))
            {
                break;
            }
            if (configRemoved)
            {
                _tprintf(
                    _T("- Sensor removed from private pool: %ls (%ls)\n"), 
                    unitArray[i].Manufacturer, 
                    unitArray[i].Description 
                    );
            }
        }
        WinBioFree( unitArray );
        unitArray = NULL;
        unitCount = 0;
    }

    if (SUCCEEDED(hr))
    {
        // Remove the database.
        hr = BioHelper::UnregisterDatabase( &databaseId );
    }
    if (SUCCEEDED(hr))
    {
        _tprintf(_T("- Private database uninstalled.\n"));
    }
    else
    {
        LPTSTR errorMessage = BioHelper::ConvertErrorCodeToString( hr );
        _tprintf(_T("*** Error - %s\n"), errorMessage );
        LocalFree(errorMessage);
        errorMessage = NULL;
    }
}

//-----------------------------------------------------------------------------

static void onAdd()
{
    WINBIO_UUID databaseId = PRIVATE_POOL_DATABASE_ID;
    WINBIO_UUID dataFormat = {};

    if (!isDatabaseInstalled( &databaseId, &dataFormat))
    {
        _tprintf(_T("*** Error - private database not installed.\n"));
        return;
    }

    WINBIO_UNIT_SCHEMA *unitArray = NULL;
    SIZE_T unitCount = 0;
    HRESULT hr = WinBioEnumBiometricUnits( 
                    WINBIO_TYPE_FINGERPRINT, 
                    &unitArray, 
                    &unitCount 
                    );
    if (SUCCEEDED(hr))
    {
        SIZE_T selectedUnit = 0;
        if (selectSensorMenu( 
                _T("Choose a sensor to add to the private pool"), 
                unitArray, 
                unitCount, 
                &selectedUnit
                ))
        {
            BioHelper::POOL_CONFIGURATION derivedConfig = {};
            hr = BioHelper::CreateCompatibleConfiguration( 
                    &unitArray[selectedUnit], 
                    &derivedConfig 
                    );
            if (SUCCEEDED(hr))
            {
                derivedConfig.DatabaseId = PRIVATE_POOL_DATABASE_ID;
                hr = BioHelper::RegisterPrivateConfiguration( 
                                    &unitArray[selectedUnit], 
                                    &derivedConfig 
                                    );
            }
        }
        WinBioFree( unitArray );
        unitArray = NULL;
        unitCount = 0;
    }
    if (SUCCEEDED(hr))
    {
        _tprintf(_T("- Sensor added to private pool.\n"));
    }
    else
    {
        LPTSTR errorMessage = BioHelper::ConvertErrorCodeToString( hr );
        _tprintf(_T("*** Error - %s\n"), errorMessage );
        LocalFree(errorMessage);
        errorMessage = NULL;
    }
}

//-----------------------------------------------------------------------------

static void onRemove()
{
    bool configRemoved = false;
    WINBIO_UNIT_SCHEMA *unitArray = NULL;
    SIZE_T unitCount = 0;
    HRESULT hr = WinBioEnumBiometricUnits( 
            WINBIO_TYPE_FINGERPRINT, 
            &unitArray, 
            &unitCount 
            );
    if (SUCCEEDED(hr))
    {
        SIZE_T selectedUnit = 0;
        if (selectSensorMenu( 
                _T("Choose a sensor to remove from the private pool"), 
                unitArray, 
                unitCount, 
                &selectedUnit
                ))
        {
            WINBIO_UUID targetDatabase = PRIVATE_POOL_DATABASE_ID;
            hr = BioHelper::UnregisterPrivateConfiguration( 
                                &unitArray[selectedUnit], 
                                &targetDatabase,
                                &configRemoved
                                );
        }
        WinBioFree( unitArray );
        unitArray = NULL;
        unitCount = 0;
    }
    if (SUCCEEDED(hr))
    {
        if (configRemoved)
        {
            _tprintf(_T("- Sensor removed from private pool.\n"));
        }
        else
        {
            _tprintf(_T("*** Error - selected sensor not a member of private pool.\n"));
        }
    }
    else
    {
        LPTSTR errorMessage = BioHelper::ConvertErrorCodeToString( hr );
        _tprintf(_T("*** Error - %s\n"), errorMessage );
        LocalFree(errorMessage);
        errorMessage = NULL;
    }
}

//-----------------------------------------------------------------------------

static bool selectSensorMenu(
    __in LPCTSTR Prompt,
    __in WINBIO_UNIT_SCHEMA *UnitArray,
    __in SIZE_T UnitCount,
    __out SIZE_T *SelectedUnit
    )
{
    if (!ARGUMENT_PRESENT(UnitArray) ||
        !ARGUMENT_PRESENT(SelectedUnit) ||
        UnitCount == 0)
    {
        return false;
    }

    _tprintf(_T("\n%s:\n\n"), Prompt);
    for (SIZE_T i = 0; i < UnitCount; ++i)
    {
        _tprintf(
            _T(" %3d - %ls (%ls)\n"), 
            (i + 1), 
            UnitArray[i].Manufacturer, 
            UnitArray[i].Description 
            );
    }

    _tprintf(_T("\nSelect sensor and press <ENTER>: "));
    TCHAR buffer[20] = {};
    HRESULT hr = StringCbGets( buffer, 20*sizeof(TCHAR) );
    _tprintf(_T("\n"));

    int selected = _tstoi( buffer );
    if (selected <= 0 ||
        selected > (int)UnitCount)
    {
        return false;
    }
    *SelectedUnit = (SIZE_T)(selected - 1);
    return true;
}

//-----------------------------------------------------------------------------

static bool isDatabaseInstalled(
    __in WINBIO_UUID *DatabaseId,
    __out WINBIO_UUID *DataFormat
    )
{
    if (!ARGUMENT_PRESENT(DatabaseId) ||
        !ARGUMENT_PRESENT(DataFormat))
    {
        return false;
    }

    bool databaseInstalled = false;
    WINBIO_STORAGE_SCHEMA *storageArray = NULL;
    SIZE_T storageCount = 0;

    if (SUCCEEDED(
            WinBioEnumDatabases( 
                WINBIO_TYPE_FINGERPRINT, 
                &storageArray, 
                &storageCount 
                )))
    {
        for (SIZE_T i = 0; i < storageCount; ++i)
        {
            if (storageArray[i].DatabaseId == *DatabaseId)
            {
                *DataFormat = storageArray[i].DataFormat;
                databaseInstalled = true;
                break;
            }
        }

        WinBioFree( storageArray );
        storageArray = NULL;
        storageCount = 0;
    }

    return databaseInstalled;
}
//-----------------------------------------------------------------------------
```



 

 




